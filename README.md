

# 🚀 Terraform AWS EC2 Provisioning

This project demonstrates **Infrastructure as Code (IaC)** using Terraform to provision an AWS EC2 instance with a secure SSH-enabled Security Group.

It is designed as a **DevOps learning project** to showcase Terraform fundamentals, AWS provisioning, and modular infrastructure design.



## 📌 Project Features

* Provision AWS EC2 instance (t2.micro)
* Create and manage Security Group (SSH access only)
* Infrastructure defined as code using Terraform
* Output public IP of the instance
* Easy deployment and teardown
* Clean and modular structure (ready for future modules)


## 🏗️ Architecture Overview

```
Terraform
   │
   ├── AWS Provider
   │
   ├── Security Group (SSH)
   │
   └── EC2 Instance (Ubuntu)
           │
           └── Public IP Output


```

## 📁 Project Structure

```
terraform-aws-ec2/
├── main.tf            # Main infrastructure definition
├── variables.tf       # Input variables
├── outputs.tf         # Output values (public IP)
├── terraform.tfvars   # Variable values
├── .gitignore         # Ignored files (state, cache)
└── README.md
```



## ⚙️ Prerequisites

Before running this project, make sure you have:
```
* Terraform >= 1.0
* AWS CLI installed
* AWS account with access keys
* Configured credentials:
```
Command
```
aws configure
```



## 🚀 Usage

### 1. Initialize Terraform

```
terraform init

```


### 2. Format code

```
terraform fmt
```



### 3. Validate configuration

```
terraform validate
```



### 4. Preview changes

```
terraform plan

```


### 5. Deploy infrastructure

```
terraform apply

```
Type `yes` when prompted.



### 6. Get EC2 Public IP

After deployment:

```
terraform output public_ip
```

Or check AWS Console.



### 7. Destroy infrastructure (cleanup)

```
terraform destroy
```



## 🔐 Security Notes

* SSH access is restricted (recommended to set your own IP in Security Group)
* Never commit AWS credentials to GitHub
* `.tfstate` file is ignored for safety



## 🧠 What I Learned

* Terraform basics (init, plan, apply, destroy)
* AWS EC2 provisioning
* Security Groups and inbound rules
* Infrastructure as Code (IaC)
* State management concepts
* Basic DevOps workflow



## 📈 Future Improvements

* Add Terraform modules (reusable EC2 module)
* Use S3 backend for remote state
* Add VPC + Subnet configuration
* Automate deployment with GitHub Actions
* Add Ansible for post-provision configuration
* Add multiple environments (dev/staging/prod)



## 👨‍💻 Author

**DevOps Learning Project**

Built for practicing:
```
* Linux
* AWS
* Terraform
* DevOps fundamentals
```


## ⭐ If you like this project

Give it a star and feel free to fork it for your own learning 🚀

