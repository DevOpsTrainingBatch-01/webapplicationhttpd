.  ********** SSK Devops**************
Select EC2 from the Services Menu
Select Launch Instance and Create an EC2 Instance. 
Choose appropriate OS. I have used AWS Linux
Create a Key Pair. (This .pem/ppk file will be the specific key whose presence will enable you to login from anywhere)
We have successfully created & launched the instance.
After initializing the EC2 Instance, we will have to connect it to the VM.
For this we have three methods:
 1. We will use the PuTTY or mobaxterm to convert
 2. If we have downloaded the .ppk or ppm file then we can directly initialize the VM on our local Machine/System.
 3. We will directly connect to the VM through the AWS platform
 I have used the 3rd method.

 After connecting with the Instance, we will run the following commands on the console:
 1. sudo su -
 2. yum update -y
 3. yum install -y httpd
 4. systemctl status httpd
 5. mkdir aws_assg3
 6. cd aws_assg3
 7. For this assignment we have created a portfolio website which we have uploaded on Github.com.
 8. Copy the Download Link for the .zip file of the portfolio
 9. using the wget command, download the zip file to the folder.
 10. unzip the master.zip file and navigate in to the ShreyasKulkarni_Portfolio-master folder using the cd command.
 11. move all the contents from the folder to “/var/www/html/”

Edit the Inbound Rules in security groups (SSH,HTTP,HTTPS)
check the status of httpd and then enable & start httpd using the following commands
  systemctl status httpd
  systemctl enable httpd
  systemctl start httpd
Now open the public ipv4 address allocated to the EC2 instance we created in new tab. We will be able to see the Portfolio Website.
