
![alt text](https://i.imgur.com/peligtC.png)

# **osTicket Project**:
## In this project I will be able to walk-through and document the installation of an open-source, web-based helpdesk ticketing system in a Microsoft Azure virtual environment.
## I will learn how to use osTicket as, an administrator, a helpdesk technician and as a customer.

## What Azure resources will be used in this project?
* Azure Virtual Machine (Windows 10)
* Azure Network Security Groups (Firewall Resources)

## What Prerequisite Software will be Required to Install and operate osTicket?

*  Windows 10 IIS
*  PHP Manager for IIS
*  RewriteAMD64
*  VC_Redist_x86
*  MySQL 5.8.62
*  osTicket
*  HeidiSQL
*  Remote Desktop

## Operating Systems Used
* Windows 10
## **Start the Process of Installing osTicket**

### Enable IIS and World Wide Web Services, as shown below.

![alt text](https://i.imgur.com/WrSuqfS.png)

### Enable CGI (which allows the installation of PHP Manager)

![alt text](https://i.imgur.com/pJPlSlB.png)

Next...Lets test to see if our web server is working correctly by opening a browser and adding "127.0.0.1" (localhost IP address): as shown below

![alt text](https://i.imgur.com/dFH4dW3.png)

If you see the above page, IIS is working fine and webpages are loading correctly.

### Next....Install PHP Mamager For IIS: 

![alt text](https://i.imgur.com/Xbc9BYa.png)

### Next....Install Rewrite_AMD64_en-US

![alt text](https://i.imgur.com/PNdROpR.png)

### Next....Create a directory folder for PHP on the local hard drive, as shown below.

![alt text](https://i.imgur.com/WK08ZCd.png)

### Next....Unzip the content of "PHP-7.3.8-nts" and empty the files into the "PHP" folder just created, as shown below.


![alt text](https://i.imgur.com/JRAg9IY.png)

### Next....Install "VC_Redist.x86"


![alt text](https://i.imgur.com/p4KBgr5.png)

### Next....Install "MySQL-5.5.62-win32"


![alt text](https://i.imgur.com/d9pJ6kn.png)

### Next....Select the "Standard Configuration", as shown below.

![alt text](https://i.imgur.com/pablUaE.png)

### Next....Create your **root password** and remember it!! You'll need to add this password in later configurations.

![alt text](https://i.imgur.com/DHUi9QD.png)

### Next....Need to add configurations inside IIS:
* Open IIS as admin
* Register PHP
* Then start installing osTicket
### Next....Open IIS as admin

![alt text](https://i.imgur.com/6lEth9p.png)

### Click on "PHP Manager", as shown above.

![alt text](https://i.imgur.com/3HndNaC.png)

### Click on "PHP is not enabled. Register new PHP version to enable PHP via FastCGI", as shown above.

### Next....Must provide the path to find the "php executable file" called **php-cgi.ext**, as shown below.

![alt text](https://i.imgur.com/8ZkLFFB.png)

### Now, browse to "PHP" folder on C: drive.  Find "php-cgi" file, as shown below.

![alt text](https://i.imgur.com/lEJqTYL.png)

### Now, go ahead and click "OK" to confirm the "php-cgi.exe" file, as shown below.

![alt text](https://i.imgur.com/jGKSOWI.png)

### "PHP" is now enabled, as shown below.


![alt text](https://i.imgur.com/BlSR7zj.png)
### Next....We need to "Restart the IIS Server" again. Do this by clicking on **VM-osTicket** (on the left) under **Connections** and then click "Restart" (on the right), as shown below.

![alt text](https://i.imgur.com/AuXJq7B.png)

### How to Restart the IIS Server?
First: Click on VM-osTicket / Second: Click on Restart 

### Next....Install osTicket

### As shown below, (starting from the right-side), open the "osTicket" zip file and "drag" (to the left), the **Upload** folder over to the **C:\inetpub\wwwroot\** folder.

![alt text](https://i.imgur.com/KpFq5Q5.png)

### Next....Rename the **Upload** folder just copied over. Rename that folder "osTicket", as shown below.

![alt text](https://i.imgur.com/IIInYXJ.png)

### Next....Restart IIS server again!

### Next....Test the "osTicket" webpage to see if it launches.
### (from the left) Click on **Site**, **Default Web Site** and select **osTicket**. Then (from the right) click on **Browse*;80**, as shown below.

![alt text](https://i.imgur.com/QNlnG9V.png)
