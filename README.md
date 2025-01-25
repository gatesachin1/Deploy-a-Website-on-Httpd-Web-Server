*********** Step to host website on Httpd server ************

----------------------------------------------
1. Login to  AWS console
2. Create ec2 instance
3. Configure security group(ssh -22 for admin only)(80 - http for normal traffic)
4. Connect to ec2 instance
3. update packages
#yum   update  -y
4. install httpd package
#yum  install  httpd   -y
#rpm   -q    httpd
5. start and enable httpd service
#systemctl   start   httpd
#systemctl   enable  httpd
6. open browser and verify default web page
http://192.168.1.5 --> output : it works ( Default httpd page )
9. host website using free website template ( https://www.free-css.com/free-css-templates)
#wget  https://www.free-css.com/assets/files/free-css-templates/download/page295/yoga.zip
#ls
#unzip  yoga.zip
#cp -rvf yoga/* /var/www/html/
10. open browser and verify
http://192.168.1.5 ( EC2-Instance Public IP )
Final output :
![image](https://github.com/user-attachments/assets/8ee63132-09f6-4017-8cf7-2d3ecb640bd3)
