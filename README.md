# thirvusoft
This repository has the details of Frappe setup commands


FRAPPE SETUP COMMANDS:

sudo apt-get update -y
sudo apt-get upgrade -y

Install Required Packages

sudo apt-get install git
sudo apt-get install python3-dev python3.10-dev python3-setuptools python3-pip python3-distutils
sudo apt-get install python3.10-venv
sudo apt-get install software-properties-common
sudo apt install mariadb-server mariadb-client
sudo apt-get install redis-server
sudo apt-get install xvfb libfontconfig wkhtmltopdf
sudo apt-get install libmysqlclient-dev

CONFIGURE SQL SERVER:
sudo mysql_secure_installation
(After the above command there will be some Yes or No question --Refer docs)

sudo nano /etc/mysql/my.cnf
sudo service mysql restart
sudo apt install curl

curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
source ~/.profile
nvm install 18

sudo apt-get install npm
sudo npm install -g yarn
sudo pip3 install frappe-bench

#Upto the above command first time execution is enough


bench init --frappe-branch version-15 frappebench1(your bench name)
cd frappebench1

bench new-site siddsite

Install ERPNext and other Apps:

bench get-app payments
bench get-app --branch version-15 erpnext
bench get-app hrms
bench --site siddsite install-app erpnext
bench --site siddsite install-app hrms #HR

bench use siddsite
bench --site siddsite add-to-hosts

bench start
![image](https://github.com/user-attachments/assets/b53102e0-4734-465d-a7a7-6bb5d9f0ce0c)
