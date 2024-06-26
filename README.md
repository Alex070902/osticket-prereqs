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
osticket has several prerequisites you must download and install
they can be found here: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6

- PHP 7.3.8
- PHP manager
- Vc redist
- My SQL 5.5
- IIS (internet information services)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In your micorsoft azure vitual machine, go to the control panel. Select "programs", then "programs and features", then "turn windows features on and off. a new window should come up
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
in this new window, scrol down to the folder called "internet information services" and check the box. Expand this folder, then do the same for "worldwide web services" and "application developmetn features". check the folder called "CGI". lastly, go to the folder called common http features and amke sure everything in ther eis checked. select "ok" (NOTE: to make sure you installed this correctly, type 127.0.0.1 in a web browser and a special webpage should show up. if this doesnt happen you may have to try reinstalling)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next download and install php manager, and the rewrite module
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a new directory in the C drive - C:\PHP, then download php 7.3.8 (extract all the files into the directory you just created, C:\PHP)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
download and instal vc redist x86
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
download mysql and launch the setup. Choose "typical setup" then check the "launch mysql instance configuration" box. when its launched, click standard configuration. create a root password (dont forget it) then click next and execute
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
now its time to register PHP with IIS. first run IIS as an administrator, then double click "php manager". thenclick "register new php version" click the 3 dots to the right and browse to the c drive in that folder where you extracted the php files. in this folder will be a file called "php.cgi". open this (note: be sure to restart iis whenever you install/ change anything)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download os ticket folder, find another folder inside called "upload". open anoter window in file explorer. go back to the c drive and find a foler called "inetpub" then "wwwroot". go back to the other window and drag the "upload" folder into the "wwwroot" folder, then rename the "upload" folder to "osticket" (restart iis)
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
back in iis, navigate to the left side, click sites > default > osticket. while "osticket" is highlighed navigate to the right and click "browse". if done properly, you should see a new osticket window pop up
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
go back to the "osticket" folder in iis and select "php manager" once again. click "enable or disable an extension" at the bottom. enabke "php_imap.dll", "php_intl.dll", and "php_opcache
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

