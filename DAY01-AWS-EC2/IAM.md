# IAM (Identity and Access management) made easy

Managing who can access wha in your AWS environment is critical, that where AWS IAM come in picture.

### What is IAM?

IAM (Identity and Access management) is a service that helps you securely control access to AWS resouces. With IAM, you can create **Users** and **Group**, Defin permissions to allow or deny acceess.

### Core IAM Components

- Users
- Groups
- Roles
- Policies
- Permissions

#### Users:
- Represent person or app that intract with AWS.

#### Groups:
- A collection of users with the same permissions.
- Create IAM Group to manage permissions for multiple users at one place.
- Group can logically organize users.
-  AWS IAM Policies can be attached to User and Group

#### Policies: 
- JSON documens that define what actions are allowed/denied
- IAM policies defines the permissions which can be assigned to Users or Group
- AWS Pprovides built in policies and it also gives us the option to create custom policies

#### Roles
- IAM role is similar to an IAM user, what the user do or can not do in AWS.
- Give permission to AWS services to access other services in AWS.

`Note: AWS IAM uses effective permissions by combining policies at group and user level. when combining if there is conflict between allow and deny, deny is always the winner`

## IAM POLICY STRUCTURE

When working with AWS Identity and Access Management (IAM), it's crucial to understand how policies are structured. IAM policies define permissions for actions on AWS resources, and they are written in JSON format. Below is a basic example of an IAM policy:

IAM Policy defines the permissions which can be assigned to user or role or group

AWS Provides built in policies and it also gives us the option to create custom policies.



        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": "*",
                    "Resource": "*"
                }
            ]
        }

## Key Components of an IAM Policy

- **version:** Specifies the policy language version, the current version is 2012-10-17
- **Statement**: 
The core element of the policy, which defines what is allowed or denied. A policy can contain a single statement or an array of Statements.

    - Effect: Whether the statement Allows or Denies access.

    - Principal (used in resource-based policies)
        - Specifies the user, account, service, or other entity that is allowed or denied access.
        - Example: "Principal": { "AWS": "arn:aws:iam::123456789012:user/pravinade" }
    - Action: 
        - Lists the actions that are allowed or denied.
        - Example: "Action": "s3:PutObject" allows uploading objects to an S3 bucket.
        - You can use wildcards like "s3:*" to allow all S3 actions.
    - Resources: 
        - list of resources to which the action apply.
        - Example: "Resource": "arn:aws:s3:::example-bucket/*" targets all objects in a specific S3 bucket.

## IAM Groups

Create IAM Groups to manage permissions for multiple users at one place

Groups can logically organize users.
AWS IAM policies can be attached to user and group






