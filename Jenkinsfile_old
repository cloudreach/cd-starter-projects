#!groovy

// ./gradlew build
// http://jenkins.dev.sterlingbackcheck.com/job/Training/job/Jai_TEST/pipeline-syntax/globals ENV Variables

def applicationName="Application-ABC"

node('linux') {
    git url: 'http://github.com/Relus-Technologies/cd-starter-projects'

    stage "TestStage1"
    withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'testCreds', passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME']]) {
        sh """#!/bin/bash
            echo ASDF > abc-\${JOB_BASE_NAME}.txt
            echo \$USERNAME \$PASSWORD
            pwd
           """
    }

    stash name: 'testArtifact', includes: "abc-${env.JOB_BASE_NAME}.txt"
    step(
            [
                    $class                              : 'S3BucketPublisher',
                    dontWaitForConcurrentBuildCompletion: false,
                    entries                             : [
                            [
                                    bucket                 : 'relus-temp',
                                    excludedFile           : '',
                                    flatten                : false,
                                    gzipFiles              : false,
                                    keepForever            : false,
                                    managedArtifacts       : true,
                                    noUploadOnFailure      : false,
                                    selectedRegion         : 'us-east-1',
                                    sourceFile             : "abc-${env.JOB_BASE_NAME}.txt",
                                    storageClass           : 'STANDARD',
                                    uploadFromSlave        : true,
                                    useServerSideEncryption: true
                            ]
                    ],
                    profileName                         : 'ArtifactPublisher ',
                    userMetadata                        : []]
    )

}

node('linux') {
    stage 'TestStage2'
    sh "pwd"
    unstash name: 'testArtifact'
}

