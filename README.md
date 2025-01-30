# DevOps_project 1
DevOps project to learn how to setup webserver and host website on ec2 

This repository contains the code for my DevOps project, which is a simple website built using HTML and deployed on an EC2 instance with Apache web server.

Table of Contents
Installation
Usage
Contributing
License
Installation
To run this website locally, you can simply clone this repository to your local machine:

bash
Copy code
git clone https://github.com/your-username/devops-project.git
Usage
Once you have cloned the repository, you can open the index.html file in your web browser to view the website.

The website displays a message that the web server has been successfully deployed on an EC2 instance, and provides a button to share the website on LinkedIn.

Contributing
If you find any issues with the website or have suggestions for improvements, feel free to submit an issue or pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

**STEPS TO DO THE PROJECT**

STEP 1: Create a EC2 Instance with the preferred AMI [E.g. Amazon Linux] and allowing https and http ports 

STEP 2: Make a ssh connect either using the Amazon connect or MobaXterm 

STEP 3: Go to the root directory by using 
```bash
sudo su
cd ~
```
STEP 4: Update the pacakage manager and Install Apache Web Server

```bash
sudo yum update
sudo yum install httpd -y
```
STEP 5:Start the Apache server
```bash
sudo systemctl enable httpd
sudo systemctl start httpd
```
STEP 6:Install git
```bash
sudo yum update
sudo yum install git -y
```
STEP 7: Navigate to wev root directory and Clone the repository
```bash
cd /var/www/html/
sudo git clone https://github.com/your-username/DevOps_project1.git
```
STEP 8: Move the file  to the root of the web  directory
```bash
sudo mv /var/www/html/DevOps_project1/* /var/www/html/
sudo rm -rf /var/www/html/DevOps_project1
```
STEP 9:Adjust Permissions of the file 
```bash
sudo chown -R apache:apache /var/www/html/
sudo chmod -R 755 /var/www/html/
```
STEP 10:Now you can access the website by entering the Public IP of your EC2 instance

**CONGRATULATIONS ON THE DEVOPS PROJECT**


                
                

