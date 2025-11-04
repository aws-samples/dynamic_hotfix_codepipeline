## Dynamic Pipeline Management for Hot-fix Solution Deployment

This pattern describes how to deploy a hot-fix to a production environment securely using dynamic pipelines. A hot-fix is typically deployed to address critical or security issues reported in a live environment, such as Production.

This pattern helps address a scenario of managing a dynamic hot-fix CodePipeline dedicated solely to deploying hot-fixes. The  hot-fix pipeline is automatically created when a hot-fix branch is created and terminated when the hot-fix branch is deleted. The solution is implemented using an AWS Service Catalog Product, which is launched or terminated based on an Amazon EventBridge rule. The AWS CodePipeline can deploy the application only once. This restriction is enforced within the AWS CodePipeline stage using a custom AWS Lambda function (Pull Request Setup).

This pattern is designed for environments with the following setup:

A [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) setup is adopted for the development workflow in the CI/CD process. The pipelines follow the deployment cycle starting from development → QA → stage → production environments. There are two long-lived git branches in the CI/CD setup with promotional deployments to environments as follows:


`develop` → Development Environment

`main` → QA → Stage(Pre-Production) → Production environments 


> Note: Please follow the AWS Prescriptive Guidance for further instructions on how to use the code sample

</n>

##  [Automate dynamic pipeline management for deploying hotfix solutions in Gitflow environments by using AWS Service Catalog and AWS CodePipeline](https://docs.aws.amazon.com/prescriptive-guidance/latest/patterns/automate-dynamic-pipeline-management-for-deploying-hotfix-solutions.html).

</n>

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

