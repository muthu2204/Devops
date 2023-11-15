#!/bin/bash
sudo su
sed 's/PasswordAuthentication no/PasswordAuthentication yes/' -i /etc/ssh/sshd_config
systemctl restart sshd
service sshd restart
useradd ec2-user
echo "1234" | passwd --stdin ec2-user
adduser ec2-user sudo
