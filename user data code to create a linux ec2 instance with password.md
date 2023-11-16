#!/bin/bash
sudo su
sed 's/PasswordAuthentication no/PasswordAuthentication yes/' -i /etc/ssh/sshd_config
systemctl restart sshd
service sshd restart
adduser ec2-user
echo ec2-user:1234 | chpasswd
adduser ec2-user sudo
apt-get update -y
apt-get install -y sshpass
