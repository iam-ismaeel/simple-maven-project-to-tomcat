***



```
This is a terraform code 
```


...
...
}

###    region = "us-east-1"
}
...
...

```
PS C:\Users\USER\3-TIER AWS-VPC-TERRAFORM PROJECT\CI-infra> terraform init

Initializing the backend...

Initializing provider plugins...
- Finding latest version of hashicorp/local...
- Finding latest version of hashicorp/aws...
- Finding latest version of hashicorp/tls...
- Installing hashicorp/local v2.5.1...
- Installed hashicorp/local v2.5.1 (signed by HashiCorp)
- Installing hashicorp/aws v5.58.0...
- Installed hashicorp/aws v5.58.0 (signed by HashiCorp)
- Installing hashicorp/tls v4.0.5...
- Installed hashicorp/tls v4.0.5 (signed by HashiCorp)

Terraform has created a lock file .terraform.lock.hcl to record the provider
selections it made above. Include this file in your version control repository
so that Terraform can guarantee to make the same selections by default when
you run "terraform init" in the future.

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.
PS C:\Users\USER\3-TIER AWS-VPC-TERRAFORM PROJECT\CI-infra>

```

#### The next is terraformplan to indicate our resources to be created.
```
Plan: 13 to add, 0 to change, 0 to destroy.
```

#### The next is terraform apply to create the resources
```
tls_private_key.rsa_4096: Creating...
aws_security_group.instance_sg[2]: Creating...
aws_security_group.instance_sg[1]: Creating...
aws_security_group.instance_sg[0]: Creating...
aws_security_group.instance_sg[3]: Creating...
aws_security_group.instance_sg[4]: Creating...
tls_private_key.rsa_4096: Creation complete after 5s [id=4940b82d802a9322d05b65ac5459613f114debba]
aws_key_pair.key_pair: Creating...
local_file.private_key: Creating...
local_file.private_key: Creation complete after 0s [id=c5d98043a7260a168807abd74dc2fe80ba182542]
aws_key_pair.key_pair: Creation complete after 1s [id=akanni]
aws_instance.public_instance["Jenkins_slave"]: Creating...
aws_instance.public_instance["Nexus_server"]: Creating...
aws_instance.public_instance["Jenkins_master"]: Creating...
aws_instance.public_instance["SonarQube_server"]: Creating...
aws_security_group.instance_sg[4]: Creation complete after 5s [id=sg-03f6d286d7d39cfd1]
aws_security_group.instance_sg[0]: Creation complete after 5s [id=sg-0045dcc3f63107f29]
aws_security_group.instance_sg[3]: Creation complete after 5s [id=sg-0a0df86fb1e784e9f]
aws_security_group.instance_sg[2]: Creation complete after 5s [id=sg-08d37f348c13559d5]
aws_security_group.instance_sg[1]: Creation complete after 5s [id=sg-0aab0790733682cae]
aws_instance.public_instance["Ansible_server"]: Still creating... [10s elapsed]
aws_instance.public_instance["Jenkins_slave"]: Still creating... [10s elapsed]
aws_instance.public_instance["Jenkins_master"]: Still creating... [10s elapsed]
aws_instance.public_instance["Nexus_server"]: Still creating... [10s elapsed]
aws_instance.public_instance["SonarQube_server"]: Still creating... [10s elapsed]
aws_instance.public_instance["Ansible_server"]: Still creating... [20s elapsed]
aws_instance.public_instance["Jenkins_slave"]: Still creating... [20s elapsed]
aws_instance.public_instance["Jenkins_master"]: Still creating... [20s elapsed]
aws_instance.public_instance["Nexus_server"]: Still creating... [20s elapsed]
aws_instance.public_instance["SonarQube_server"]: Still creating... [20s elapsed]
aws_instance.public_instance["Ansible_server"]: Still creating... [30s elapsed]
aws_instance.public_instance["Jenkins_slave"]: Still creating... [30s elapsed]
aws_instance.public_instance["Nexus_server"]: Still creating... [30s elapsed]
aws_instance.public_instance["Jenkins_master"]: Still creating... [30s elapsed]
aws_instance.public_instance["SonarQube_server"]: Still creating... [30s elapsed]
aws_instance.public_instance["Ansible_server"]: Creation complete after 34s [id=i-0d706083d88f0b496]
aws_instance.public_instance["SonarQube_server"]: Creation complete after 35s [id=i-02db206abaa355de5]
aws_instance.public_instance["Jenkins_slave"]: Creation complete after 35s [id=i-080bece0f71582306]
aws_instance.public_instance["Nexus_server"]: Creation complete after 35s [id=i-0d699ca2b8b800e2a]
aws_instance.public_instance["Jenkins_master"]: Creation complete after 35s [id=i-0d77628fbb552aab4]

Apply complete! Resources: 13 added, 0 changed, 0 destroyed.
```

