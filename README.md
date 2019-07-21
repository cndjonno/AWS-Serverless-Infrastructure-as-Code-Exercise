# AWS-Serverless-Infrastructure-as-Code-Exercise
An exercise using terraform (for infrastructure as code) to deploy a API Gateway instance which passes requests to Lambda for processing

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

## Disclaimer
Note: When using Terraform ***DO NOT*** commit your Secret and AUthenitication AWS Keys into your github account - bots will crawl this and steal access to your account.
You should Use IAM (Identity and Access Management) to create a new User and attach only Policies for the services that you are about to provision with terraform. Use the set of Keys in CIRCLECI environment variables and pass them in via that, instead of committing them to your repo.

## ####Part 1### Steps
### Let's setup the #########:
1) Look up how to setup your local AWS CLI and configure your AWS security keys in the credientials file 
2) Install Terraform
3) What do terraform init, plan, apply commands do?
4) Setup a S3 bucket using terraform and view the bucket has shown up in AWS in your browser.
5) Delete the S3 bucket from your terraform codebase and add a Lambda function. You'll need to bundle the zip file for the lambda code to deploy successfully.
6) Maybe configure API Gateway - I'd suggest you put it in a file called apigateway.tf in the same folder as your lambda terraform code.
7) Add a S3 bucket in your terraform code and then manually upload the zip file into it using AWS CLI or in your browser.


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

