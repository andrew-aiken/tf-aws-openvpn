# tf-aws-openvpn

## Prerequisites
Terraform v0.14.5 or newer
AWS CLI installed

## Running
```terraform init```
```terraform apply```<br>
Select if you want pihole server
Type 'yes' to run script<br>
To shutdown run ```terraform  destroy``` and follow the above steps.

## Defaults
Change key pair being used in variables.tf (ec2_ssh_key)<br>

|Service|Username|Password|
--- | --- | ---
|VPN Admin|openvpn|passwd|
|VPN User|foo|bar|
|Pihole||PiholeAdminPassword|