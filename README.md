# Ansible_testing_project_01
Using my projects in udacity as a reference I will test the instalation of software remotely using a ansible playbook


# Overview

The main focus for this project is to prepare the machine with the required software to run the application, for this purpose ansible will be use to install nginx


### Project Tasks

This project goal is to do a small example how to use this technology:
* Create a new user
* Provide roles to the new user
* Install an EC2 instance
* Install ansible
* Install nginx software using ansible playbook

## Pre-requisites

1. Create the user
2. Create a policy with the permissions to create an EC2 isntance
3. Configure the user in aws cli in your standalone environment
4. Create a KeyPair (For this case I use "jb_aws_keypair.pem")

## Instructions

### 1. Running the infraestructure in a EC2 instance

a. Configure the user in your aws cli

b. Create an EC2 instance using the Wizard

c. Connect to the EC2 instance and clone this repository in the EC2 instance
```bash
chmod 400 jb_aws_keypair.pem
ssh -i "jb_aws_keypair.pem" ubuntu@ec2-56-23-79-154.us-west-2.compute.amazonaws.com
git clone https://github.com/JoseBerrocal/Ansible_testing_project_01.git
```

d. Install Ansible
```bash
cd Ansible_testing_project_01
sh install_ansible.sh
```

e. Update "nginx_ansible/roles/nginx/vars/main.yaml" with external IP of the EC2 instance

f. Run Ansible
```bash
cd nginx_ansible
ansible-playbook -i inventory main.yaml
```

d. Access the URL of the EC2 instance, the output can be the following
![alt text](https://github.com/JoseBerrocal/Ansible_testing_project_01/blob/master/images/ansible_project_01_outoput.png)


## Enhancements

To improve the project it will be required to deploy several VM, install differet softwares.