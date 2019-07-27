# AWS-Serverless-Infrastructure-as-Code-Exercise
An exercise using terraform (for infrastructure as code) to deploy a API Gateway instance which passes requests to Lambda for processing.

## The Task
In this exercise you're tasked to make a repository that:
- configures aws resources by writing your [infrastructure as code](https://martinfowler.com/bliki/InfrastructureAsCode.html).
- stores the infrastructure code within a GitHub repository.

## What will you learn?
- Write your infrastructure as code with terraform.
- locally store your API keys in a AWS Credentials file for local development.

## Disclaimer
Note: You should ***NEVER*** commit your AWS Access Key and Secret key into your github repository - bots will crawl this and steal access to your account. _Guard these keys with your life._ If you do make a mistake you can Deactivate the key in the AWS Console, and issue yourself a new one.

## Let's setup the basics
1) Look up how to setup your local AWS CLI and configure your AWS security keys in the credientials file.
2) [Install Terraform](https://learn.hashicorp.com/terraform/getting-started/install.html)
3) Look up what terraform init, plan, apply commands do? [Getting Started With Terraform](https://learn.hashicorp.com/terraform/getting-started/build.html)
4) Setup a S3 bucket (in the console first if you've never done it then) using terraform and view the bucket has shown up in AWS in your browser.
5) Delete the S3 bucket from your terraform codebase and a Simple Notification Service instance [SNS](https://aws.amazon.com/sns/). 
6) Run terraform plan and see what the plan output says - how many things are deleted, how many are added?
7) Ask your neighbor where they're at, and help them to complete the setup because the next bit we need small teams!

## Lets setup something a bit more complicated:
To build the full infrastructure as code for the Serverless API endpoint we shall form a group! There are several peices and you'll be better off working together. 

The following tasks need to be done to make a working solution. I've shuffled the instructions so together you have to work out:
- how it hangs together - DIAGRAM!
- how to independently work on bits without depending on each other too much.
- try rate each step on complexity 1, 3, 5, 8. 
- hint: use a whiteboard!
- Work out who has done what - someone new should focus on terraform or something they've used before if possible.

Steps:
 - A: ZIP the lambda code and commit it into your Github repo where the Lambda code lives (lookup the zip format AWS requires).
 - B: A API Gateway resource defined in terraform.
 - C: Connect the API Gateway to the Lambda in terraform.
 - D: Make the CircleCI job push the Lambda zip file into a S3 bucket anytime someone commits.
 - E: A Lambda function resource defined in terraform.
 - I: Make a branch on this repository to hold all infrastructure as code artifacts.
 - F: Check the terraform repository does not have AWS Secret + Access keys (if it does revoke them immediately).
 - G: Make a S3 bucket that the Lambda code lives in.
 - H: Make code for the lambda function to run (use your previous JSON response lambda or make a simple hello world one).
 - J: Get all team members Added to CodersUK on Github

Note: Realistically you'd want CircleCI to checkout the code, make the zip then upload it to S3. The zipping process is actually overly fiddly so I've left this as optional - it's really just icing on the cake so lets bake the cake and not burn it first.
Z - Make CircleCI ZIP the files as part of the build job and remove the zip file from the github repo.

## Whats next?
- Chill (eh really? I thought you came here to learn).
- I can't beleive you finished early, maybe you're actually entired to Chill! Nice work!
- Look up what Terraform Backend State is, why you might you use it?
