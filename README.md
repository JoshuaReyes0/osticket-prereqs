<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com/watch?v=txUV5oDcH-0)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Prerequisites </h2>

  - osTicket Installation Files: https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/hOwksO2.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<p>
Create a Virtual Machine on Azure:
  
  - Access Azure Portal.
  - Click on "Virtual Machine (VM)."
</p>
<br />

<p>
<img src="https://i.imgur.com/AEbOzPy.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/V7Ol72s.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/g3ytOjB.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure Virtual Machine:
  
  - Create a Resource Group named: LAB-osTicket.
  - Name the Virtual Machine: VM-osTicket.
  - Select Windows 10 VM with 2-4 VCPU.
  - Username: labuser, Password: [Specify an easy password].

</p>
<br />

<p>
<img src="https://i.imgur.com/DX7kk4e.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/RiE7dwk.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> 
<img src="https://i.imgur.com/t6KqsXY.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/b7oAEwh.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Access VM and Configure IIS:

  - Copy the VM's IP Address.
  - Open Remote Desktop Connection and connect to Windows 10.
  - In Control Panel, open Programs.
  - Click on “Turn windows feature on or off”.
  - Toggle on CGI, Common HTTP Features, and IIS Management Console.

</p>
<br />
<p>
<img src="https://i.imgur.com/WnPUZqn.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/3sbRNlN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/UIymXXo.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/niHkKbN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/v9rFq9j.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>   
</p>
<p>
Install PHP and Rewrite Module:
  
  - Install PHP Manager for IIS and Rewrite Module.
  - Create directory C:\PHP.
  - Download and unzip PHP 7.3.8 to C:\PHP.
  - Install VC_redist.x86.exe.

</p>
<br />

<img src="https://i.imgur.com/utvmACz.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/8I9QtVP.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/3zUPjjh.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/zlsXDh6.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>  
</p>
<p>
Install MySQL:
  
  - Install MySQL 5.5.62 with a typical setup.
  - Launch Configuration Wizard, configure MySQL with Standard settings, and set the password to "Password1."
</p>
<br />

<img src="https://i.imgur.com/6WUbRj8.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/BScLtim.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/VcJZT9V.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/l7LSI7A.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/rrZCS9o.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/r3FUELP.png" height="20%" width="20%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/jhqF59b.png" height="60%" width="=60%" alt="Disk Sanitization Steps"/> 
</p>
<p>

Configure IIS for PHP and Install osTicket:

  - Open IIS as an Admin.
  - Register PHP in IIS.
  - Reload IIS.
  - Install osTicket v1.15.8.
  - Extract "upload" folder to c:\inetpub\wwwroot.
  - Rename "upload" to "osTicket."

</p>
<br />

<img src="https://i.imgur.com/Js4ZDJ4.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/595PqgW.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> 
</p>
<p>
  
  - In IIS go to "Browse *.80 (http)".
  - Now you are in the osTicket webpage server.


<img src="https://i.imgur.com/T8CmVVQ.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/BScLtim.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/XaQjsUY.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/UEF0rBf.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>  
</p>
<p>

  Enable PHP Extensions:
  
  - Open IIS (Default -> osTicket-> Double-click PHP Manager).
  - Click on “Enable or disable an extension”.
  - Enable php_imap.dll, php_intl.dll, php_opcache.dll.

</p>
<br />

<img src="https://i.imgur.com/o2f64JX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> 
</p>
<p>

  - Now continue with the osTicket webpage set up.


</p>
<br />
<p>
<img src="https://i.imgur.com/sKGpBuB.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/ZHFQEHo.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> 
<img src="https://i.imgur.com/ZYFWA9r.png" height="20%" width="20%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/rQtk5ic.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>  <img src="https://i.imgur.com/eXYpOEV.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/0rTihc4.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/YvKABoN.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/qUNNljQ.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/uDGQh7c.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/iNrSvMo.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
</p>
<p>
Configure osTicket:
  
  - Rename ost-sampleconfig.php to ost-config.php.
  - Set permissions for ost-config.php (Disable inheritance -> Remove All -> New Permissions -> Everyone -> All).
  - Set up osTicket in the browser (Name Helpdesk, Create an Email).


</p>
<br />

<img src="https://i.imgur.com/X08j6mY.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/EQX7OuE.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/IujOumX.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/TdN2U2Z.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/lpHa7WN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> 
</p>
<p>

Install and Configure HeidiSQL:

  - Install HeidiSQL.
  - Open Heidi SQL, create a new session (root/Password1), and connect.
  - Create a database called "osTicket."


</p>
<br />
<p>
<img src="https://i.imgur.com/cGKzyko.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/tsjZmlg.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> 
</p>
<p>

Complete osTicket Setup:

  - Return to osTicket and finish the setup.
  - MySQL Database: osTicket, MySQL Username: root, MySQL Password: Password1.
  - Click "Install Now!"

Verify Installation:

  - Browse to your help desk login page: http://localhost/osTicket/scp/login.php.
</p>
<br />
