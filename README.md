"Deploying a Static Website on AWS EC2 Using Apache HTTPD"

Short Intro: In this project, I have hosted a website on an AWS EC2 instance using Apache HTTPD. By launching an EC2 instance, installing and configuring the Apache web server, and deploying a static website, you will gain hands-on experience in setting up a web server on AWS. Additionally, you will learn how to replace a custom webpage with a free website template for quicker deployment.
Project Objectives:
•	Deploying a web on httpd server
Prerequisites:
•	Basic knowledge of AWS services, particularly EC2.
•	Understanding of HTTP and web servers and Basic Linux command.
1.	Login to AWS Console
o	Login to your AWS account using your credentials and Launch EC2 Instance
2.	Connect to EC2 Instance
o	Once the EC2 instance is running, select it from the EC2 dashboard.
o	Click on Connect and follow the SSH connection instructions to connect to your instance.
3.	Update Packages
o	Once connected to your EC2 instance, run the following command to update the system:
# yum update -y
4.	Install HTTPD Package
o	Install the Apache HTTP server using the following command:
# yum install httpd -y
o	Verify the installation:
# rpm -q httpd
5.	Start and Enable HTTPD Service
o	Start the Apache service:
# systemctl start httpd
o	Enable the Apache service to start on boot:
# systemctl enable httpd
6.	Open Browser and Verify Default Web Page
o	Open your browser and navigate to the EC2 instance’s private IP:
http://192.168.1.5
o	The default Apache HTTPD page should display with the message: "It works!"
7.	Create Custom Webpage
o	Change to the web directory:
# cd /var/www/html/
o	Edit the index.html file:
# vim index.html
o	Replace the content with your custom HTML:
html
Copy
<html>
    <head>
        <title>Pune</title>
    </head>
    <body bgcolor="yellow">
        <h1>Welcome to Apache HTTPD Web Server</h1>
    </body>
</html>
o	Save and exit (:wq).
8.	Open Browser and Verify Custom Web Page
o	Open your browser and navigate to the EC2 instance’s private IP:
http://192.168.1.5
o	Verify that your custom web page is displayed.
9.	Remove Custom Web Page and Host Website Using Free Template
o	Remove the custom index.html and all other files:
# rm -rvf /var/www/html/*
o	Download a free website template from https://www.free-css.com/free-css-templates:
# cd
# wget https://www.free-css.com/assets/files/free-css-templates/download/page295/yoga.zip
o	Unzip the downloaded template:
# unzip yoga.zip
o	Copy the template files to the web directory:
# cp -rvf yoga/* /var/www/html/
10.	Open Browser and Verify the Hosted Website
o	Open your browser and navigate to the EC2 instance's public IP (public IP address of your EC2 instance):
http://<EC2-Public-IP>
o	Verify that the new website (using the free template) is successfully hosted.
________________________________________
Summary: In this project, I launched an EC2 instance, installed and configured Apache HTTPD, created a custom webpage, and then replaced it with a free website template. The website was verified both locally on the EC2 instance and through the public IP, making it accessible over the web.

