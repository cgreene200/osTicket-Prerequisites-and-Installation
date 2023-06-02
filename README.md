
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

### Enable IIS, World Wide Web Services and CGI, as shown below.
### Go to the "Control Panel" and click on "Programs", as shown below.
![alt text](https://i.imgur.com/EUfrVXm.png)
### Click on "Turn Windows Features on and off", as shown below.
![alt text](https://i.imgur.com/zFpG2Kq.png)
### Click on "Internet Information Services" (IIS), as shown below.
![alt text](https://i.imgur.com/2QfELPc.png)
![alt text](https://i.imgur.com/jRr9Vt9.png)

![alt text](https://i.imgur.com/ggFws5N.png)
### Enabling CGI, allows the installation of PHP Manager.

### Next...Lets test to see if our web server is working correctly by opening a browser and adding "127.0.0.1" (localhost IP address): as shown below

![alt text](https://i.imgur.com/dFH4dW3.png)

### If you see the above page, IIS is working fine and webpages are loading correctly.

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

![alt text](https://i.imgur.com/TDQMmTF.png)

### Click on "PHP Manager", as shown above.

![alt text](https://i.imgur.com/LnQZxRT.png)

### Click on "Register new PHP version", as shown above.

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
### First: Click on VM-osTicket / Second: Click on Restart 

### Next....Install osTicket

### As shown below, (starting from the right-side), open the "osTicket" zip file and "drag" (to the left), the **Upload** folder over to the **C:\inetpub\wwwroot\** folder.

![alt text](https://i.imgur.com/KpFq5Q5.png)

### Next....Rename the **Upload** folder just copied over. Rename that folder "osTicket", as shown below.

![alt text](https://i.imgur.com/IIInYXJ.png)

### Next....Restart IIS server again!

### Next....Test the "osTicket" webpage to see if it launches.
### (from the left) Click on **Site**, **Default Web Site** and select **osTicket**. Then (from the right) click on **Browse*:80(http)**, as shown below.

![alt text](https://i.imgur.com/QNlnG9V.png)

### After clicking on "Browse*:80(http)", if you see the osTicket webpage image below, your configurations so far, are correct. If you "DO" see errors at this point, you must start troubleshooting.

![alt text](https://i.imgur.com/clQ8Ffe.png)

Next....Enable a few extensions in IIS. Search for **IIS**, click on **Site**, **Default Web Site** and **osTicket**. **PHP Manager** and scroll down to **PHP Extensions** and click on **Enable or disable an extension** as shown below.

![alt text](https://i.imgur.com/2xdABgT.png)

### Extensions that need to be enabled:  (Afterwards, refresh the webpage)
* php_imap.dll
* php_intl.dll
* php_opcache.dll

#### Click on listed extensions and move to the **right** to click on **Enable**, as shown below.

![alt text](https://i.imgur.com/HPTAalY.png)

### Next....Edit the "ost-sampleconfig.php" file, located using the following path:
### C:\inetpub\wwwroot\osTicket\include
### Find the file **ost-sampleconfig.php** and change it to **ost-config.php**

### Next....Set Permissions on the **ost-config.php** file so "everyone" has full access.

**Right-click on this file -> go down to "Properties" -> click on "Security" -> Click on**
**"Advanced" and then click on "Disable Inheritance" and then "Remove all inherite permisions from this object".**

### Now click on "Add" to add a permission. Enter "Everyone", as shown below:

![alt text](https://i.imgur.com/OTYlhvt.png)

### Hit "OK" and give them "Full Control".  Then, hit "Apply" -> "OK" and then "OK".

### Next....Continue configuring "osTicket" in the browser, fictitious information will be used, as shown below.

![alt text](https://i.imgur.com/XQYhKBe.png)
* **Helpdesk Name:**  John Doe's Helpdesk
* **Default Email:**  JD@helper.com


![alt text](https://i.imgur.com/TEzkt8C.png)
* **First Name:**  John
* **Last Name:**   Doe
* **Email Address:**  JD@helper.com
* **Uername:**     dj
* **Password:**    (create your own)
* **Retype Password:

### Next....Before we can configure the "Database Settings" below, we must first install "HeidiSQL". (HeidiSQL is a database client for MySQL) and allows us to connect to the SQL server that osTicket is going to use.

![alt text](https://i.imgur.com/gio1EQd.png)

### Next....Install "HeidiSQL Setup"


![alt text](https://i.imgur.com/I3bkNRg.png)

![alt text](https://i.imgur.com/4yHtlCr.png)


![alt text](https://i.imgur.com/BJ8bGgV.png)
### Select "New" to create a new database, as shown above.

![alt text](https://i.imgur.com/mhCijTA.png)
### This is the password that we setup when we installed "MySQL"
### Apply that password and then hit "Open", as shown above.


![alt text](https://i.imgur.com/2rPrK3d.png)
### Now, we can see our "mysql" server, as shown above.

### Next....We need to fill out the remainder of the "osTicket" Database Settings: As shown below.
![alt text](https://i.imgur.com/NFZS5tr.png)

### **MySQL Username:**  root
### **MySQL Password:**  (This password was created in MySQL)
### **MySQL Database:**  (Please Pay Attention Here!)
### This database must be created in "HeidiSQL", as shown below.

![alt text](https://i.imgur.com/9RNhydj.png)

![alt text](https://i.imgur.com/u1U6P5A.png)

### Give this new database the name "osTicket", as shown above.


![alt text](https://i.imgur.com/L0XDODH.png)
### We see above that "osTicket" was created without any errors!!!
### Next....Now, we can add the "MySQL Database" to "osTicket" Database Settings, as shown below:

![alt text](https://i.imgur.com/Rc0zcqM.png)
### Next....Finish installing osTicket by clicking on "Install Now".


![alt text](https://i.imgur.com/6EZf60n.png)

### Congratulations!!........osTicket installed without any errors!!

### One last thing!!!...we have to go back into the "osTicket" folder and delete a folder called "Setup".
### Here's the path again!  C:\inetpub\wwwroot\osTicket
### Find the "Setup" folder and delete it.

### Lastly, we need to find the "ost-config.php" file and set the permissions back to "read only".
### The path to this file is: C:\inetpub\wwwroot\osTicket\include
