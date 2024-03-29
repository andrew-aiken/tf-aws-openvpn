# tf-aws-openvpn
## Prerequisites
Terraform v0.14.5 or newer
<br>
AWS CLI installed

## Running
```terraform init```
```terraform apply```<br>
Select if you want Pihole server
Type 'yes' to run script<br>
To shutdown run ```terraform  destroy``` and follow the above steps.

## Defaults
Change key pair being used in variables.tf (ec2_ssh_key)<br>

|Service|Username|Password|
--- | --- | ---
|VPN Admin|openvpn|passwd|
|VPN User|foo|bar|
|Pihole||PiholeAdminPassword|

## Whats happening?

The `vpn_ec2` ec2 creates a [OpenVPN](https://openvpn.net/) server which assigns the DNS name of the next server `pihole_ec2`.

The DNS server `pihole_ec2` installs [Pihole](https://pi-hole.net/) a DNS blackhole (removing unwanted dns queries) and [Unbound](https://docs.pi-hole.net/guides/dns/unbound/
) which recursively makes dns queries to the root servers.

*Root → TLD → Authoritative → IP Address*
