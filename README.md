<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket v1.15.8
- PHP 7.3.8
- MySQL 5.5.62
- PHP Manager for IIS
- URL Rewrite Module
- HeidiSQL

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create Azure Virtual Machine
- Access the VM
- Prepare Installation Files
- Enable IIS with CGI
- Install PHP Manager and Rewrite Module
- Install and Configure PHP
- Install MySQL
- Configure IIS
- Install osTicket
- Access osTicket in Browser

<h2>Installation Steps</h2>

<h3>1. Create Azure Virtual Machine </h3>
 
  - Resource Group --> Create new: osTicket
- VM Name: osticket-vm
- Region: Canada Central
- Image: Windows 10 Pro Version 22H2
- Size: Standard D2s v3 2 vCPUs 8 GiB RAM (or anything with at least 2 vCPUs)
- Set Username & Password
- Check Licensing
- Click Review and Create

<p>
<img src="https://i.imgur.com/qYUei7w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>


</p>
<br />

<p>
<img src="https://i.imgur.com/tMu5It8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>

  <h3>2. Connect to the VM </h3>
 
  - Use Remote Desktop to connect to osticket-vm with your credentials.
</p>
<img src="https://i.imgur.com/rVyeCMm.png" "/>
</p>
<br />

<p>
  <h3>3. Prepare Installation Files </h3>
 
- Download osTicket-Installation-Files.zip (https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download) to the desktop.
- Extract the contents to a folder named osTicket-Installation-Files.

<img src="https://i.imgur.com/jnpRMyU.png" />
</p>
<br />

<p>
  <h3>4. Install IIS with CGI </h3>
 
- Open Control Panel > Programs > Turn Windows features on or off.
- Enable: Internet Information Services Under World Wide Web Services > Application Development Features: check CGI.

<img src="https://i.imgur.com/FcaCYbm.png"/>
<img src="https://i.imgur.com/lhkyk0x.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>5. Install PHP Manager and URL Rewrite Module </h3>
 
 From the osTicket-Installation-Files folder:
- Install PHPManagerForIIS_V1.5.0.msi.
- Install rewrite_amd64_en-US.msi.

<img src="https://i.imgur.com/bD2USwo.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>6. Set Up PHP </h3>
 
- Create a directory: C:\PHP.
- Extract php-7.3.8-nts-Win32-VC15-x86.zip into C:\PHP.
- Install VC_redist.x86.exe.

<img src="https://i.imgur.com/RUSqqpw.png"/>
<img src="https://i.imgur.com/rkgZchS.png"/>
<img src="https://i.imgur.com/XOBm0X9.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>7. Install MySQL </h3>
 
Run mysql-5.5.62-win32.msi.
- Choose Typical Setup.

After installation, launch the Configuration Wizard:
- Select Standard Configuration.
- Set Username & Password.
- Finish Installation.

<img src="https://i.imgur.com/bkkBVFY.png"/>
<img src="https://i.imgur.com/WnKjQHQ.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>8. Configure PHP in IIS</h3>
 
- Open IIS Manager through Windows search bar and run as administrator.
- Double-click PHP Manager.
- Click Register new PHP version.
- Browse to C:\PHP\php-cgi.exe and select it.
- Restart IIS: In the right pane, click Restart under Manage Server.

<img src="https://i.imgur.com/NkXDKPP.png"/>
<img src="https://i.imgur.com/BN31CL5.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>9. Deploy osTicket</h3>
 
- Extract osTicket-v1.15.8.zip from the osTicket-Installation-Files folder.
- Copy the upload folder to C:\inetpub\wwwroot.
- Rename upload to osTicket.

<img src="https://i.imgur.com/rEGYIAb.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>10. Access osTicket in Browser</h3>
 
In IIS Manager:
- Expand Sites > Default Web Site > osTicket.
- In the right pane, click *Browse :80.

The osTicket setup page should open in your default browser.

<img src="https://i.imgur.com/0SJjP5U.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>11. Enable PHP Extensions</h3>
 
- In IIS Manager, navigate to Sites > Default Web Site > osTicket.
- Double-click PHP Manager.
- Click Enable or disable an extension.

Enable the following extensions:
- php_imap.dll
- php_intl.dll
- php_opcache.dll

Refresh the osTicket setup page in your browser to confirm the extensions are enabled.

<img src="https://i.imgur.com/HgujPme.png"/>
<img src="https://i.imgur.com/VTh3VPl.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>12. Configure osTicket</h3>
 
Rename the configuration file:
- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Set permissions for ost-config.php:
- Right-click the file > Properties > Security > Advanced.
- Click Disable inheritance and remove all inherited permissions.
- Click Add > Select a principal > type Everyone > Check Names > OK.
- Grant Full control permissions to Everyone.
- Click OK to apply changes.

<img src="https://i.imgur.com/ngU5IFw.png"/>
<img src="https://i.imgur.com/rNjLbye.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>13. Install HeidiSQL and Create Database</h3>
 
- Install HeidiSQL from the osTicket-Installation-Files folder.
- Open HeidiSQL and create a new session:
- Enter Username & Password.
- Connect to the session.
- Right-click in the left pane and select Create new > Database.
- Name the database osTicket.

<img src="https://i.imgur.com/SIS58Ra.png"/>
<img src="https://i.imgur.com/oCXRRir.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
  <h3>14. Complete osTicket Web Setup</h3>
 
In the osTicket setup page in your browser:

- Fill in the required fields:
- Helpdesk Name
- Default Email
- Admin Username
- Admin Password
- Database Settings:
- MySQL Database: osTicket
- MySQL Username
- MySQL Password
- Click Install Now!

<img src="https://i.imgur.com/tHqDp0f.png"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
