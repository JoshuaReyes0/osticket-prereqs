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

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/1GWpZIQ.png" height="60%" width="60%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/2MnoIgB.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> 
</p>
<p>
Create a Virtual Machine on Azure:
  
  - Access Azure Portal.
  - Click on "Virtual Machine (VM)."
</p>
<br />

<p>
<img src="https://i.imgur.com/UkSi34R.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/jUYkSx3.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/214KlhN.png" height="40%" width="40%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/tyncXHS.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>   
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
<img src="https://i.imgur.com/TZ1a2hG.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/TaZDQdk.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> 
<img src="https://i.imgur.com/6ujviyy.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/pU8BSMI.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>  <img src="https://i.imgur.com/GwkZC9P.png" height="50%" width="50%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/v6vYXMB.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/DVz6mI8.png" height="30%" width="30%" alt="Disk Sanitization Steps"/> <img src="https://i.imgur.com/grFwrLi.png" height="30%" width="30%" alt="Disk Sanitization Steps"/>
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
  
  - Install MySQL 5.5.62 with typical setup.
  - Launch Configuration Wizard, configure MySQL with Standard settings and set the password to "Password1."
</p>
<br />
