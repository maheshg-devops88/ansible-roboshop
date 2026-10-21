# Ansible-Roboshop-Automation

Ansible code for deploying the Infrastructure in AWS and configuring the Roboshop e-commerce application.

# Deploying ec2 instances requirement 

> Configure IAM role with required permission and assign to ansible-controller instance which is required to deploy ec2 instances.

# Deploying ec2 instances and application services 

> Use below ansible command to deploy the ec2 instances 

 ansible-playbook -i inventory.ini roboshop.yaml -e 'instances=["mongodb","redis","mysql","rabbitmq","catalogue","user","cart","shipping","payment","frontend"]'

> To deploy the application code using ansible use below command for each roboshop service

ansible-playbook -i inventory.ini mongodb.yaml
