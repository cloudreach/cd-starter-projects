#!groovy

def thiDepVersion = ''


node('linux') {
    checkout([
            $class                           : 'GitSCM',
            branches                         : [
                    [
                            name: '*/master'
                    ]
            ],
            doGenerateSubmoduleConfigurations: false,
            extensions                       : [],
            submoduleCfg                     : [],
            userRemoteConfigs                : [
                    [

                            url: 'http://github.com/Relus-Technologies/cd-starter-projects'
                    ]
            ]
    ])
    gitCommit = sh(returnStdout: true, script: 'git rev-parse HEAD').trim()

    sh "echo ${gitCommit}"

}