# CodeDeploy
* Create an 'AppSpec.yml' file at the root of your deployable package
* Create/Use a service role that has permissions to CodeDeploy/Ec2 resources
* Create/Use an instance profile that CodeDeploy/Ec2 resources
* Install CodeDeploy Agent on instance that will be deployed on

## Links
* AppSpec (General)
http://docs.aws.amazon.com/codedeploy/latest/userguide/app-spec-ref.html
* AppSpec (File Structure)
http://docs.aws.amazon.com/codedeploy/latest/userguide/app-spec-ref-structure.html
* AppSpec (Lifecycle Hooks)
http://docs.aws.amazon.com/codedeploy/latest/userguide/app-spec-ref-hooks.html
* Tutorial
https://aws.amazon.com/getting-started/tutorials/deploy-code-vm/