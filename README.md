# AWS-Serverless-Infrastructure-as-Code-Exercise
An exercise using terraform to deploy a API Gateway instance which passes requests to Lambda for processing

## The Task
- stores the infrastructure code within GitHub.
- configured aws resources with [infrastructure as code](https://martinfowler.com/bliki/InfrastructureAsCode.html).
- uses [CircleCI](https://circleci.com) to deploy updates to the infrastructure using [continuous delivery](https://martinfowler.com/bliki/ContinuousDelivery.html).
- Uses backend state in AWS S3 bucket

## Use Infrastructure as Code to Create the API and Lambda.
We should create the API Gateway and Lambda with Terraform (or another Infrastructure as code tool) so this is managable just like code using pull requests and reviews. When we change the infrastructure code this should run through a continuous delivery pipeline and update AWS resources just like we would with code.
Note: When using Terraform ***DO NOT*** commit your Secret and AUthenitication AWS Keys into your github account - bots will crawl this and steal access to your account.
You should Use IAM (Identity and Access Management) to create a new User and attach only Policies for the services that you are about to provision with terraform. Use the set of Keys in CIRCLECI environment variables and pass them in via that, instead of committing them to your repo.
