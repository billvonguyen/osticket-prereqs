<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services
- Install Web Platform Installer
- Install MySQL
- Install C++ Redistributable
- Configure Permissions and Install osTicket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/22eLvvN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. 1st step is to Enable Internet Information Services, so in order to do so you must navigate to control panel and click on "Programs and Features" then click on "Turn Windows features on or off". Scroll down until you see "Internet Information Services" and check mark the empty box to turn the feature on.
</p>
2. There's also further prerequisites as well. You'll want to expand "World Wide Web Services" folder and "Application Development" folder then checkmark the empty box by "CGI".

<img src="https://i.imgur.com/ecaHMqF.png" height="50%" width="50%"/>

3.  Once you're done with that you'll then want to expand "Common HTTP Features" and checkmark "HTTP Redirection" and "WebDAV Publishing".

<img src="https://i.imgur.com/0Ej81GX.png" height="50%" width="50%"/>
<br />

<p>
4. Download and install the PHP for Internet Information Services from the following link. 
 
  https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view
  
  <img src="https://i.imgur.com/Mr4dClI.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

5. Download and install the rewrite module from the following link.

  https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view

<img src="https://i.imgur.com/COtj9TU.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

6. Create a directory for PHP, so create a new folder in your Windows C Drive and name it PHP.

<img src="https://i.imgur.com/AC8Vcm3.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

7. Download PHP from the following link and extract the files of the zip folder into the "PHP" folder you created earlier.
   
   https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view

8. Download and install C++ Redistributable from the following link.

  https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view
<img src="https://i.imgur.com/FHjgv4C.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
   
9. Download and install MYSQL from the following link.

  https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view

  Proceed with next and click on a typical install.
  
<img src="https://i.imgur.com/O7gQ2PP.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

10. Run Internet Information Services as Admin.
<img src="https://i.imgur.com/WBK952C.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

11. Run and register PHP Manager from within Internet Information Services.
<img src="https://i.imgur.com/qB92POc.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/yqcz10T.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
You'll find the executable PHP file within your PHP folder that you created earlier.
<img src="https://i.imgur.com/3AQuiz2.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

12. Download the OsTicket zip file from the following link and extract and move the upload folder into c:\inetpub\wwwroot then rename upload folder to osTicket.

https://drive.google.com/file/d/1VeVXKlzHDRjeaVUL99ptq7qYbrbXdFxJ/view

<img src="https://i.imgur.com/4TbfhFB.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

13. Reload Internet Information Services and then go to "Sites","Default","OsTicket" and on the right click “Browse *:80”.

<img src="https://i.imgur.com/W2OUkKC.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

14. Navigate back to Internet Information Services and double click on PHP Manager.

<img src="https://i.imgur.com/Kgmdr2C.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  Then click on enable or disable extensions, enable the following extensions:
  
-php_imap.dll

-php_intl.dll

-php_opcache.dll

<img src="https://i.imgur.com/wAzcdxD.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

Refresh the osTicket site in your browser and check that your changes were made.

15. Navigate to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php within your directory and rename ost-sampleconfig.php to ost-config.php

<img src="https://i.imgur.com/3w8I0b4.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

16. Right click the file go to properties, security, advanced, disable inheritance, remove all permissions, add permissions, select a principle, type in Everyone within the textbox, check names and hit ok, then click full control and click ok, apply, and ok.


<img src="https://i.imgur.com/VGo5lsX.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

17. Go back to the browser and click on continue in the osTicket site then register with a anonymous username, email, and password. I highly recommend taking note of it so you don't forget!

<img src="https://i.imgur.com/unz7lya.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

18. Download and install HeidiSQL from the following link.

https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit

Run HeidiSQL and login using the username and password you created for MySQL.

<img src="https://i.imgur.com/xsgvB2p.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

From there, create a new session, connect to the session, and create a database called "osTicket".

<img src="https://i.imgur.com/mkavvLC.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

Make sure that your MySQL username and password is the same when you register it into the osTicket browser.
And lastly enter "osTicket" in the MySQL Database textbox and click "Install Now".

<img src="https://i.imgur.com/hLkxFQZ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

If everything is done correctly then the installation should be a success and you'll receive a confirmation webpage as shown below.

<img src="https://i.imgur.com/YQ5Urfi.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

  





  




    
  


