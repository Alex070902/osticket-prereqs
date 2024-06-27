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

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/68b14ad5-49b8-43a2-8040-e3b2c9b3c2c5)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/adddf09f-cd79-4092-8d99-cc3e5327d328)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/f69942f0-b84b-42e7-94cb-5db87096d4c9)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/55c303b6-19c9-4bb9-9b23-981d40b4ca8c)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/fe779976-afe1-4616-a5d0-96c3f1af3bf5)






Now its time to register PHP with IIS. First run IIS as an administrator, then double click "php manager". Then click "register new php version" click the 3 dots to the right and browse to the c drive in that folder where you extracted the php files. In this folder will be a file called "php.cgi". Open this (note: be sure to restart iis whenever you install/ change anything)

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/509c5562-7d22-4cc8-815d-8ef6293d443e)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/16b5c862-7743-457a-b3d5-9aa77dd27c77)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/d60e2609-d9ef-45d6-a9b2-2c28583ebfa3)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/a02915b5-180a-4d79-836a-69f73e9491ee)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/74dfed75-ad14-4c83-a60e-5e1e52ab0931)


Download the osticket folder, find another folder inside called "upload". open another window in file explorer. Go back to the C drive and find a folder called "inetpub" then "wwwroot". go back to the other window and drag the "upload" folder into the "wwwroot" folder, then rename the "upload" folder to "osticket". (restart iis)

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/f490130a-374e-4bd3-9984-1ca63a579c7a)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/10a1665b-9aab-4ff4-b316-f7c44cdd6c17)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/52c2b382-3d70-4abe-830a-eb1748fe7456)


Back in iis, navigate to the left side, click sites > default > osticket. While "osticket" is highlighed navigate to the right and click "browse". If done properly, you should see a new osticket window pop up.

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/c901f519-135e-4ea4-800c-6dfd89317759)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/fc4efb9a-2f53-4089-8014-126c05b46134)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/5df2f50a-d502-4555-a13f-71dcb6e0170e)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/6d564d63-8c28-4810-aa41-d14d16f457cf)



Some of the extensions arent enabled, so go back to the "osticket" folder in iis and select "php manager" once again. Click "enable or disable an extension" at the bottom. Enabke "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Once you do this refresh the page in osticket to make sure the changes stick.

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/ba8f1373-42ad-4028-aa05-8596726665af)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/01046368-c709-4def-a99c-9db216ffd665)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/39c2f633-ccc5-4611-a85e-6a0196a09e2c)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/ac682c0d-8f8d-48fb-8290-111ae2987fd0)


Go back to the wwwroot folder and find your "osticket" folder. In this folder is another one called include. Double click it and find a file called "os-sampleconfig.php", change the name to "os-config.php". (it may be a good idea to change permissions for certain users)

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/cdcb3036-2025-4693-bcdc-b3529b903919)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/959d4435-26c5-4629-806c-95d383bab320)

You should still be in the first screen in the os ticket window (most of the extensions should be enabled too) after this, youll be brought to a screen where youll have to fill out a buch of information. At the bottom however, under "database settings" youll need to setup your database using heidisql

![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/ac415835-7800-47b8-beae-4fc159e5bb78)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/c20d403d-a834-4bda-837e-9bec6532a750)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/182c1856-ca69-4102-b018-6482d260f36f)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/6d29c549-dde5-4d3b-a6b7-4950c8161d5d)
![image](https://github.com/Alex070902/osticket-prereqs/assets/173719378/98cf070f-4abc-457e-9f66-26b06e6cd73c)

Download and install heidiSql, then open it. Navigate to the bottom left of the screen wher eit says "new", and login using the same information as you did in  mysql, then click open. finish setting up in the browser by creating a database in heidisql. click "install" at the bottom
