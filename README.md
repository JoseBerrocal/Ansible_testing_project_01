# Ansible_testing_project_01
Testing the instalation of software remotely using a book


# Overview

The main focus for this project is to prepare the machines with the required software to run the application, for this purpose ansible will be use


### Project Tasks

This project goal is to do a small example how to use this technology:
* Create a new user
* Provide roles to the new user
* Install a VM
* Install the software requried using books in ansible


## Project Plan

* [Trello board for the project](https://trello.com/b/cdioDvZb/building-a-ci-cd-pipeline)

## Pre-requisites

1. Create the user
2. Create a policy with the following permissions:   
    - iam:CreateInstanceProfile
    - iam:DeleteInstanceProfile
    - iam:PassRole
    - iam:DeleteRolePolicy
    - iam:RemoveRoleFromInstanceProfile
    - iam:CreateRole
    - iam:DeleteRole
    - iam:PutRolePolicy
    - iam:AddRoleToInstanceProfile
3. Add the following policies to a user:
    - AmazonEC2FullAccess
    - AWSCloudFormationFullAccess
    - Policy from point 2.
4. Configure the user in aws cli in your standalone environment
6. Create a KeyPair (For this case I use "jb_aws_keypair.pem")

## Instructions

* Architectural Diagram 

### 1. Running the infraestructure in a standalone environment

a. Clone this repository in your local environment

b. Configure the user in your aws cli

c. Execute the following commands
```bash
cd infraestructure
```

d. Test the installation of the software
```bash
(.able-infra)
```


## Enhancements

To improve the project it will be required to deploy several VM, install differet softwares.