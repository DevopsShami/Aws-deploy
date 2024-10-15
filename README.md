Testing the project locally
Clone this project
git clone https://github.com/DevopsShami/Aws-deploy.git
Setup the following environment variables - (.env) file
DOMAIN= ""
PORT=8080
STATIC_DIR="./client"

PUBLISHABLE_KEY=""
SECRET_KEY=""

Note : We need to create this keys in stripes

Initialise and start the project
npm install
npm run start
Set up an AWS EC2 instance


Create an IAM user & login to your AWS Console
Access Type - Password
Permissions - Admin
Create an EC2 instance
Select an OS image - Ubuntu
Create a new key pair & download .pem file
Instance type - t2.micro


Connecting to the instance using ssh
ssh -i instance.pem ubunutu@<IP_ADDRESS>
Configuring Ubuntu on remote VM 

Updating the outdated packages and dependencies
sudo apt update

Install Git - Guide by DigitalOcean
Configure Node.js and npm - Guide by DigitalOcean

Deploying the project on AWS
Clone this project in the remote VM
git clone https://github.com/DevopsShami/Aws-deploy.git
Setup the following environment variables - (.env) file
DOMAIN= ""
PORT=8080
STATIC_DIR="./client"

PUBLISHABLE_KEY=""
SECRET_KEY=""
For this project, we'll have to set up an Elastic IP Address for our EC2 & that would be our DOMAIN

Initialise and start the project
npm install
npm run start

NOTE - We will have to edit the inbound rules in the security group of our EC2, in order to allow traffic from our particular port

Project is deployed on AWS 🎉
