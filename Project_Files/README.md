<br>

## This README file contains:
-Overview of the project <br>
-Use cases for the pipeline<br><br>

## Project Overview
This CI/CD platform deploys AWS infrastructure using Terraform IaC. It deploys an Auto-Scaling Group with a desired and minimum capacity of 2 instances and a maximum capacity of 3 instances. It also deploys a security group, shared between both instances, allowing outbound internet traffic and inbound traffic from port 22 and 80.<br><br>

Before creation of the pipeline, I utilized the AWS CLI to create a new S3 bucket to save the Terraform state file.<br><br>
 

When accessing the EC2 instances through searching the public IPV4 address they run a simple PHP script that displays a webpage informing the user that the CI/CD pipeline is operational. <br><br>

When changes are made on Terraform, it automatically provisions these changes when the pipeline is ran in Gitlab and saves the changes to a state file on an S3 bucket.

## Use Cases
This project will function as a template for deploying AWS infrastructure and monitoring those changes using S3 buckets.  