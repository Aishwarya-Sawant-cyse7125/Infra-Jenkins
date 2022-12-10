# infra-jenkins
Repository for Jenkins Ansible Playbooks

## Run Command for setting up networking

```
ansible-playbook -v -e "aws_profile=root aws_region=us-east-1 instance_type=t2.micro \
ami_id=ami-id \
email_id=example@gmail.com \
domain_name=example.domain.com sub_domain=example.subdomain.com \
group_name=grpname ec2_key_name=keyname \
setup-playbook.yml --private-key ./private_key.pem
```

## Delete command for detroying the networking components

```ansible-playbook -v -e "env=jenkins aws_profile=root aws_region=us-east-1" delete-playbook.yml ```