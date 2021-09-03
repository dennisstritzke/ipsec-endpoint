# IPsec Endpoint Deployment
This repo provides an Ansible Playbook the spin up a Strongswan IPsec tunnel between two machines. This is mainly used to test [dennisstritzke/ipsec_exporter](https://github.com/dennisstritzke/ipsec_exporter).

1. Create two VMs
1. Add the public IP and private subnet of each VM to the `inventory`
1. `ansible-playbook -i inventory strongswan.yml`
1. Execute `ipsec status` on one of the VMs to see the established tunnel