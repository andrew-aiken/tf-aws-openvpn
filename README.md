# tf-aws-openvpn

## Prerequisites
Terraform v0.14.5<br>
AWS CLI installed


## Running
```terraform init```<br>
```terraform apply```<br>
Select if you want pihole server<br>
Type 'yes' to run script<br><br>
To shutdown run ```terraform  destroy``` and follow the above steps.

## Defaults
Change key pair being used in variables.tf (ec2_ssh_key)
Default OpenVPN login: openvpn : passwd
OpenVPN user login: foo : bar
Default Pihole password: PiholeAdminPassword