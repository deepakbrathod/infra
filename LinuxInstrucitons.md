On Amazon Linux

Install Python3 and Upgrade PIP
	sudo yum install python37 -y
	sudo rm /usr/bin/python
	sudo ln -s /usr/bin/python3 /usr/bin/python
	sudo rm /usr/bin/pip
	sudo ln -s /usr/bin/pip3 /usr/bin/pip
	curl -O https://bootstrap.pypa.io/get-pip.py
	python get-pip.py --user
	sudo pip install --upgrade pip
	pip install ansible --user

For Terraform installation
	TERRAFORM_VER=`curl -s https://api.github.com/repos/hashicorp/terraform/releases/latest |  grep tag_name | cut -d: -f2 | tr -d \"\,\v | awk '{$1=$1};1'`
	TERRAFORM_VER="0.15.5"
	TERRAFORM_VER=0.14.9
	wget https://releases.hashicorp.com/terraform/${TERRAFORM_VER}/terraform_${TERRAFORM_VER}_linux_amd64.zip
	sudo yum -y install unzip
	unzip terraform_${TERRAFORM_VER}_linux_amd64.zip
	sudo mv terraform /usr/local/bin/
	terraform version
	terraform -install-autocomplete
	source ~/.bashrc
	
	TERRAFORM_VER=0.12.0
	TERRAFORM_VER=0.14.9

Instaling Docker-ce
	sudo yum install -y yum-utils device-mapper-persistent-data lvm2
	sudo yum -y install curl wget unzip awscli aws-cfn-bootstrap nfs-utils chrony conntrack jq ec2-instance-connect socat
	sudo amazon-linux-extras enable docker
	sudo yum -y install docker
	sudo systemctl enable --now docker
	sudo usermod -aG docker $USER
	newgrp docker
	
	mkdir terraform-docker-lab
	cd terraform-docker-lab
	
URL problem
sudo vi /usr/libexec/urlgrabber-ext-down
sudo vi /usr/bin/yum

Change python to python2



Installing Posgress
From <https://www.how2shout.com/linux/install-postgresql-13-on-aws-ec2-amazon-linux-2/> 

sudo tee /etc/yum.repos.d/pgdg.repo<<EOF
[pgdg13]
name=PostgreSQL 13 for RHEL/CentOS 7 - x86_64
baseurl=https://download.postgresql.org/pub/repos/yum/13/redhat/rhel-7-x86_64
enabled=1
gpgcheck=0
EOF

sudo yum update


sudo yum install postgresql13 -y





.ssh Vi authorized_keys


ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCwtMpT8kSxdS0FAzHx2T7e586hUarhBptH56O6arx0WWXpN0rcaW2A7IabtYuHrOswW46wQBZbivS9+Umg5SdNMSH9/154u2rNZ1a2z8fu3Qr4BTTEWM4zsNofku8++GiucyP36fwn1/JJW8whqNo6wHGy4BgVmHj2f9NO8iIJOLZ7nrDEdqTNHvqEJpennCG4Gvv0qC+WNMv2LmfQQ8LrcOvT5/oRttJMYProOmDfhmwB4paOlm60nqlZ0i+8XbTWrjaiBQgI9TrmR9w+ay+OCrmO5pt9+lquCUyehWlcB85+PBJd9RU0HajBoD7jFhoe7mlqoVKTpJpEU0JTzUhl root@ip-10-223-50-157.ec2.internal

From <https://teams.microsoft.com/multi-window/?agent=electron&version=21110108720> 


![image](https://user-images.githubusercontent.com/7494853/184548653-d47cea63-5185-4008-a8b2-085559c8f6cc.png)
