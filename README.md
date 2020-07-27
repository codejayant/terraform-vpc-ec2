# terraform-vpc-ec2
Use Terraform to create VPC and EC2 infrastructure in AWS


## Setup

### Create PEM File
Run following command in source directory

`aws ec2 create-key-pair --key-name my-first-ec2-instance --region us-west-2 --query 'KeyMaterial' --output text > my-first-ec2-instance.pem`


## Execute Terraform

1. To validate the terraform configuration
`terraform plan --var-file=production.tfvars`

2. To create the infrastructure
`terraform apply --var-file=production.tfvars`

3. To delete the infrastructure
`terraform destroy --var-file=production.tfvars`
