apt-get update
apt-get install apache2 -y
service apache2 start
rm /var/www/html/*
cd /var/tmp/
git clone https://gitlab.com/devops722546/webpage
cd webpage/
mv * /var/www/html/
