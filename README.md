![image](https://github.com/user-attachments/assets/ae1a5f9f-a042-484e-8931-012856a93e02)

This repository contains configurations and files for deploying an NGINX server on an aws ec2 instance using packer, ansible, and terraform. Before deployment, you will need:

AWS CLI
Packer
Terraform
An SSH key pair
Git

aws configure can be used to set the aws cli with appropriate crednetials for communication with aws

packer init ansible-web.pkr.hcl can be used to install required plugins

packer build ansible-web.pkr.hcl can be used to build the custom AMI

the variables.pkr.hcl file variable can be altered to change the username for the AMI

in order to deploy with terraform, we can use:

terraform init to initialize

terraform validate to validate the configuration

terraform plan to review the resources that will be created

terraform apply and a confirmation 'yes' to carry out the planning file

once launched, you can verify the deployment by sshing into the instance, and viewing it via its outputted public ip address

please note that the ec2 will be created in us-west-2

terraform destroy can be used as a simple way to clean up resources
