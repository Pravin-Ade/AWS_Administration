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









