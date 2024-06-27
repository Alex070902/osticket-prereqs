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
Osticket has several prerequisites you must download and install,
they can be found here: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


- PHP 7.3.8
- PHP manager
- Vc redist
- My SQL 5.5
- IIS (internet information services)
- HeidiSQL

<h2>Installation Steps</h2>

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/1fc2f41b-575c-4f67-8bd5-7aa2dce516f4)
![Screenshot 2024-06-27 100321](https://github.com/Alex070902/osticket-prereqs/assets/173719378/97e06a30-23cc-40f9-bc03-24a3a6898517)


In your micorsoft azure vitual machine, go to the control panel. Select "programs", then "programs and features", then "turn windows features on and off. a new window should come up

![Screenshot 2024-06-27 100450](https://github.com/Alex070902/osticket-prereqs/assets/173719378/bce4b90a-3cd0-412f-8f15-1dad7dd01518)
![Screenshot 2024-06-27 100530](https://github.com/Alex070902/osticket-prereqs/assets/173719378/434dfdf0-6d6b-4ca2-99dc-145e4ecee6c8)
![Screenshot 2024-06-27 100645](https://github.com/Alex070902/osticket-prereqs/assets/173719378/b7e92593-c6a7-4c6b-86f7-b1cc52fbd7de)
![Screenshot 2024-06-27 112225](https://github.com/Alex070902/osticket-prereqs/assets/173719378/0cf2c70a-3455-4577-8f6c-97c70f6fc0b8)




In this new window, scroll down to the folder called "internet information services" and check the box. Expand this folder, then do the same for "worldwide web services" and "application development features". Check the folder called "CGI", then go to the folder called "common http features and make sure everything in there is checked. Select "ok" (NOTE: To make sure you installed this correctly, type 127.0.0.1 in a web browser and a special webpage should show up. If this doesnt happen you may have to try reinstalling)


Next download and install php manager, and the rewrite module.

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/0ed92754-f07e-456e-a160-bcf4fd1103d4)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/8584fe86-02e3-444b-bf05-b7b3bd43118b)


Create a new directory in the C drive (C:\PHP) then download php 7.3.8 (extract all the files into the directory you just created, C:\PHP)

Download and instal vc redist x86

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/d6972426-a38f-4ecb-823a-0a9b9b9cfd84)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/f7548d74-b86a-426e-9590-b84753631a35)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/36970389-2155-4cac-880f-e81164ac0ae0)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/a1776b13-a85d-4be3-a51e-ebcb2aa8f4ca)



Download Mysql and launch the setup. Choose "typical setup" then check the "launch mysql instance configuration" box. When it's launched, click standard configuration. Create a root password (dont forget it) then click next and execute.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now its time to register PHP with IIS. First run IIS as an administrator, then double click "php manager". Then click "register new php version" click the 3 dots to the right and browse to the c drive in that folder where you extracted the php files. In this folder will be a file called "php.cgi". Open this (note: be sure to restart iis whenever you install/ change anything)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download os ticket folder, find another folder inside called "upload". open anoter window in file explorer. go back to the c drive and find a foler called "inetpub" then "wwwroot". go back to the other window and drag the "upload" folder into the "wwwroot" folder, then rename the "upload" folder to "osticket". (restart iis)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Back in iis, navigate to the left side, click sites > default > osticket. While "osticket" is highlighed navigate to the right and click "browse". If done properly, you should see a new osticket window pop up.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to the "osticket" folder in iis and select "php manager" once again. Click "enable or disable an extension" at the bottom. Enabke "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Once you do this refresh the page in osticket to make sure the changes stick.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Go back to the wwwroot folder and find your "osticket" folder. In this folder is another one called include. Double click it and find a file called "os-sampleconfig.php", change the name to "os-config.php". (it may be a good idea to change permissions for certain users)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You should still be in the first screen in the os ticket window (most of the extensions should be enabled too) after this, youll be brought to a screen where youll have to fill out a buch of information. at the bottom however, under "database settings" youll need to setup your database using heidisql
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install heidiSql, then open it. Navigate to the bottom left of the screen wher eit says "new", and login using the same information as you did in  mysql, then click open. finish setting up in the browser by creating a database in heidisql. click "install" at the bottom
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

