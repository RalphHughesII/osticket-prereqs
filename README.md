<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />




<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>


To begin this tutorial create a virtual machine in Microsoft Azure.  

- Create a Resource Group
 - Create a Windows 10 Virtual Machine using at least 2 virtual CPUs
 - Log into to the VM using windows remote desktop

Install / Enable IIS in Windows.
<p>

 - Right click the start menu
 - Click run and type control
 - Click Programs and select turn windows features on or off under Programs and Features
 - Scroll down to Internet Information Services and click the box next to this
 - locate and expand World Wide Web Services, expand Application Development Features and select CGI features
 
<img src="https://i.imgur.com/qoti6AN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

 - Collapse this window and expand common HTTP Features.  Make sure everything is checked inside and click ok.

 <img src="https://i.imgur.com/PQUv2aK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Download and Install PHP Manager from the installation folder 
(https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)


Download and Install Rewrite Module from the installation folder
(https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

Create directory for C:\PHP on local hard drive

- Navigate to C: drive, right click,select new and folder
- Name new folder - PHP

 <img src="https://i.imgur.com/trekTA3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 Download PHP 7.3.8 from the installation folder
 (https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

 - Extract all contents into PHP folder on C: drive


 Download and install VC_redist.x86.exe from the installation folder
 (https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)


Download and install MySQL 5.5.62 from the installation folder
(https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

- Select typical installation 
-  After installation select stadard configuration andinstall as Windows Service
-  Create a password and click execute

Open IIS as an Admin

- Click on start, type IIS and right click on Internet Information Services and click run as administrator

Register PHP from within IIS

- Open PHP Manager
- Select Register New PHP Version
- Navigate and open PHP folder on C: drive and select php-cgi
- Click open, then ok
- Navigate to Home section of IIS and click restart button on upper right side of window. 



Install osTicket v1.15.8

- Download and install osTicket from the installation folder
  (https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)
- Extract and copy upload folder to c:\inetpub/wwwroot

<img src="https://i.imgur.com/9fZ6ZiM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

<img src="https://i.imgur.com/j0ZGbDz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Reload IIS 

- Open IIS, Stop and Start the Server

Navigate to sites, Default, osTicket

-  Click "Browse *.80" on the right corner of the window

   <img src="https://i.imgur.com/zQVJjIA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  osTicket should open.  Notice that some extensions are not enabled.

  - Navigate to IIS, sites, Default, osTicket
  - Open PHP Manager
  - Click Enable or disable an extension

         - Enable: php_imap.dll
         - Enable: php_intl.dll
         - Enable: php_opcache.dll

- Refresh osTicket

<img src="https://i.imgur.com/3HFaI3Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Rename: ost-config.php

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<img src="https://i.imgur.com/L10JFrG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Assign Permissions: ost-config.php

- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All

<img src="https://i.imgur.com/a8F2g8f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



  
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
