# Jenkins

## Configuration
* Can be managed by administrator
## Plugins
* Huge plugin eco-system
* Common plugins aws, beanstalk, git
## Slaves
* Can be grouped by label ie. linux, .net, windows
## Pipeline DSL
* Must be named `Jenkinsfile` and located at the root of the repo
* Based on groovy
* Supports 95% of groovy functionality
  * Do not use .each loops (Not supported) use C style for loops instead
## Links
* Pipeline Step Reference
    * https://jenkins.io/doc/pipeline/steps/
* Jenkins Pipeline Tutorial
    * https://github.com/jenkinsci/pipeline-plugin/blob/master/TUTORIAL.md#triggering-manual-loading
* Jenkins Pipeline Best Practices
    * https://github.com/jenkinsci/pipeline-examples/blob/master/docs/BEST_PRACTICES.md