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

<h2>List of Prerequisites</h2>

- PHP v7.2 or greater
- MYSQLi extension for PHP


<h2>Installation Steps</h2>


![Screen Shot 2024-10-09 at 9 16 11 PM](https://github.com/user-attachments/assets/e94b1771-41fb-499a-8ef2-274b5db019ea)



Create an Azure Virtual Machine,using a Windows 10 image,with 2 to 4 vCPUs




![Screen Shot 2024-10-09 at 9 25 53 PM](https://github.com/user-attachments/assets/c65cbf23-8fe8-48bd-b1f6-e67b1afd2b4d)



![Screen Shot 2024-10-09 at 9 28 43 PM](https://github.com/user-attachments/assets/d16d826e-619b-411a-9ac9-78e2b6980be0)



</p>
<p>
  <br />
Use the public IP address along with the user name and password in Azure to log into the virtual machine with remote desktop
</p>
<br />

![Screen Shot 2024-10-09 at 9 37 26 PM](https://github.com/user-attachments/assets/cb15b77a-a702-403c-9cd0-7bb669491bd9)

![Screen Shot 2024-10-09 at 9 38 31 PM](https://github.com/user-attachments/assets/1c101653-386e-4dbb-a986-9febf12c6763)

Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”

<br />


![Screen Shot 2024-10-09 at 9 41 24 PM](https://github.com/user-attachments/assets/6cd695a9-3587-4a24-b6f2-8bd529124866)

Install / Enable Internet Information Services in Windows WITH CGI

World Wide Web Services -> Application Development Features -> MAKE SURE CGI IS CHECKED



![Screen Shot 2024-10-09 at 9 48 17 PM](https://github.com/user-attachments/assets/8ab906bb-d2e6-441d-8757-0bf1a494266e)

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)


![Screen Shot 2024-10-09 at 9 49 10 PM](https://github.com/user-attachments/assets/67258359-8cfb-43ad-9570-33f1975e4894)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)



![Screen Shot 2024-10-09 at 9 56 12 PM](https://github.com/user-attachments/assets/10f47ce5-14f0-4088-a714-abc2de011180)

Create the directory PHP in the c drive and then from the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
