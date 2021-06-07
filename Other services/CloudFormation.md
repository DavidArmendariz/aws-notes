# Infrastructure as Code

* Manual work will be very tough to reproduce:
  * In another region
  * In another AWS account
  * Within the same region if everything was deleted
* Wouldn't it be great if all our infrastructure was code?
* That code would be deployed and create/update/delete our infrastructure

## What is CloudFormation

* CloudFormation is a declarative way of outlining your AWS infrastructure for any resources
* Then CloudFormation creates those for you, in the right order, with the exact configuration that you specify

## Benefits

* Infrastructure as code
  * No resources are manually created, which is excellent for control
  * The code can be version controlled for example using git
  * Changes to the infrastructure are reviewed through code
* Cost
  * Each resources within the stack is tagged with an identifier so you can easily see how much a stack costs you
  * You can estimate the costs of your resources using the CloudFormation template
  * Savings strategy: in dev, you could automation deletion of templates at 5PM and recreated at 8AM, safely
* Productivity
  * Ability to destroy and re-create an infrastructure on the cloud on the fly
  * Automated generation of diagram for your templates
  * Declarative programming (no need to figure out ordering and orchestration)
* Separation of concern: create many stacks for many apps, and many layers

## How CloudFormation works

* Templates have to be uploaded in S3 and then referenced in CloudFormation
* To update a template, we can't edit previous ones, we have to re-upload a new version of the template to AWS
* Stacks are identified by a name
* Deleting a stack deletes very single artifact that was created by CloudFormation

## Deploying CloudFormation templates

* Manual way:
  * Editing templates in the CloudFormation Designer
  * Using the console to input parameters
* Automated way:
  * Editing templates in a YAML file
  * Using the AWS CLI to deploy the templates
  * Recommended way when you fully want to automate your flow

## CloudFormation Building Blocks

* Templates components
  * Resources: your AWS resources declared in the template
  * Parameters: the dynamic inputs for your template
  * Mappings: the static variables for your template
  * Outputs: references to what has been created
  * Conditionals: list of conditions to perform resource creation
  * Metadata
* Template helpers:
  * References
  * Functions
  
## StackSets

* Create, update, or delete stacks across multiple accounts and regions with a single operation
* Administrator account to create StackSets
* Trusted accounts to create, update, delete stack instances from StackSets
* When you update a stack set, all associated stack instances are updated throughout all accounts and regions
