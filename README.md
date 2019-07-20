# AWS-Serverless-Infrastructure-as-Code-Exercise
An exercise using terraform to deploy a API Gateway instance which passes requests to Lambda for processing

## The Task
In this exercise you're tasked to make a ######## that:
- stores the infrastructure code within GitHub.
- configures aws resources with [infrastructure as code](https://martinfowler.com/bliki/InfrastructureAsCode.html).
- uses [CircleCI](https://circleci.com) to deploy updates to the infrastructure using [continuous delivery](https://martinfowler.com/bliki/ContinuousDelivery.html).
- Uses backend state in AWS S3 bucket

## What will you learn?
- Write your infrastructure as code with terraform
- security share API keys for your AWS account with CircleCI to be used by Terraform.
- locally store your API keys in a AWS Credentials file for local development.
- Continuous Delivery of Infrastructure changes using CircleCI.

## ####Part 1### Steps
### Let's setup the #########:
1) 
2) 
3) 

We should create the API Gateway and Lambda with TerCrraform (or another Infrastructure as code tool) so this is managable just like code using pull requests and reviews. When we change the infrastructure code this should run through a continuous delivery pipeline and update AWS resources just like we would with code.
Note: When using Terraform ***DO NOT*** commit your Secret and AUthenitication AWS Keys into your github account - bots will crawl this and steal access to your account.
You should Use IAM (Identity and Access Management) to create a new User and attach only Policies for the services that you are about to provision with terraform. Use the set of Keys in CIRCLECI environment variables and pass them in via that, instead of committing them to your repo.

### Lets setup the API:
1) 
2) 
3) 

## Whats next?
At this point perhaps you should buddy up with another developer and do one of:
- Discuss whats been built or what their ######### hobby is.
- Link the API to the frontend exercise one of you has already completed.
- Chill (eh really? I thought you came here to learn).

## Links to another project

