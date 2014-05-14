ansible-demo-RootConf2014
=========================

ansible demo for rootconf 2014 workshop

Install ansible and boto:

sudo pip install ansible

sudo pip install boto


export following variables:

export AWS_ACCESS_KEY="key"

export AWS_SECRET_KEY="secret"

export ANSIBLE_HOSTS="/ansible-demo/ansible" 

About the Ansible Playbook:

* Create 1 t1.micro instance
* Edit security group to allow :22 and :80
* Create ELB
* Add the instance to ELB
* Install HTTPD
* Copy the index.html to new instance
* Check the the remote server status by http check and string match

Execute the demo playbook:

ansible-playbook -vvvv -i hosts provision_install.yaml
