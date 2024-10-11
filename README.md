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
![Screen Shot 2024-10-10 at 11 34 46 PM](https://github.com/user-attachments/assets/6fb96e57-afb8-42dd-beb1-ec41c3b89b8d)
![Screen Shot 2024-10-10 at 11 35 40 PM](https://github.com/user-attachments/assets/fc19ac4c-2aa4-4d30-a4bf-6dcec467cb07)



Install / Enable Internet Information Services in Windows WITH CGI

World Wide Web Services -> Application Development Features -> MAKE SURE CGI IS CHECKED



![Screen Shot 2024-10-09 at 9 48 17 PM](https://github.com/user-attachments/assets/8ab906bb-d2e6-441d-8757-0bf1a494266e)

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)


![Screen Shot 2024-10-09 at 9 49 10 PM](https://github.com/user-attachments/assets/67258359-8cfb-43ad-9570-33f1975e4894)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)



![Screen Shot 2024-10-09 at 9 56 12 PM](https://github.com/user-attachments/assets/10f47ce5-14f0-4088-a714-abc2de011180)

Create the directory PHP in the c drive and then from the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder



![Screen Shot 2024-10-09 at 9 57 46 PM](https://github.com/user-attachments/assets/426ff51b-72a3-410c-9597-eaabbb6446c1)


From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.



![Screen Shot 2024-10-09 at 10 03 43 PM](https://github.com/user-attachments/assets/0fc9d067-6f5d-4ae8-94fc-a898ad8dd84e)


From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->Launch Configuration Wizard (after install) ->Standard Configuration ->



![Screen Shot 2024-10-09 at 10 07 13 PM](https://github.com/user-attachments/assets/a820af00-9f5e-44d2-bc7d-97297782e568)


Open IIS as an Admin



!![Screen Shot 2024-10-09 at 10 09 25 PM](https://github.com/user-attachments/assets/ad4c1e61-b48e-42bd-aa2d-658b9269e5e0)



![Screen Shot 2024-10-09 at 10 10 12 PM](https://github.com/user-attachments/assets/00b8671c-813b-4070-bab5-3b93829359eb)



Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

![Screen Shot 2024-10-10 at 11 45 06 PM](https://github.com/user-attachments/assets/1e701098-6c06-4367-bf0b-65edb3fc735f)

![Screen Shot 2024-10-10 at 11 45 23 PM](https://github.com/user-attachments/assets/caab19dc-e76f-496f-892a-d7163c1d0000)

Reload IIS (open IIS,stop and start the server)


![Screen Shot 2024-10-09 at 10 12 58 PM](https://github.com/user-attachments/assets/398326ee-49d1-402c-9fa6-8df707137134)

![Screen Shot 2024-10-09 at 10 19 31 PM](https://github.com/user-attachments/assets/1f8c6f32-a61d-4cf9-9476-45a17f6e2a69)


![Screen Shot 2024-10-09 at 10 23 48 PM](https://github.com/user-attachments/assets/1bce8a57-fe3f-42ea-8a19-de0169111ae9)

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”


![Screen Shot 2024-10-10 at 9 53 54 PM](https://github.com/user-attachments/assets/0704cb4f-97b6-4bc5-8064-453bcdd07041)


![Screen Shot 2024-10-09 at 10 28 19 PM](https://github.com/user-attachments/assets/8c847038-2106-4635-a09c-cc293173fc38)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

![Screen Shot 2024-10-11 at 12 02 29 AM](https://github.com/user-attachments/assets/286123d8-6142-4a80-ad95-cc4990a194ef)
![Screen Shot 2024-10-11 at 12 10 54 AM](https://github.com/user-attachments/assets/87a70292-8f58-4081-afed-82fa0eaff109)
![Screen Shot 2024-10-11 at 12 11 12 AM](https://github.com/user-attachments/assets/d5a53313-4a9c-4b4c-ac7b-92ba5708b6e9)

![Screen Shot 2024-10-10 at 9 58 41 PM](https://github.com/user-attachments/assets/660dcfbd-c06c-48f9-896d-0e628c69f02d)


![Screen Shot 2024-10-09 at 10 53 42 PM](https://github.com/user-attachments/assets/2319dec1-90fd-4dc4-9246-c5f72f3e56e9)


Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php


![Screen Shot 2024-10-09 at 10 56 28 PM](https://github.com/user-attachments/assets/2be77322-628d-420e-b73d-bb1e779f9b1b)


![Screen Shot 2024-10-09 at 10 59 05 PM](https://github.com/user-attachments/assets/25c75b96-efdf-4984-b45b-069370ad248c)


![Screen Shot 2024-10-09 at 11 00 16 PM](https://github.com/user-attachments/assets/be2a9298-ab9e-409e-a602-4a3fa4dcbf71)




Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All


![Screen Shot 2024-10-10 at 10 07 00 PM](https://github.com/user-attachments/assets/25d1e1ad-3181-4da2-bf27-73e3431080b4)


![Screen Shot 2024-10-09 at 11 05 37 PM](https://github.com/user-attachments/assets/cf60e675-7cca-4f43-91c1-ffbdb2783228)


![Screen Shot 2024-10-09 at 11 08 02 PM](https://github.com/user-attachments/assets/549f1a84-f87d-41bc-8a2b-30ec9ca89595)

Open Heidi SQL
Create a new session and Connect to the session


![Screen Shot 2024-10-09 at 11 11 37 PM](https://github.com/user-attachments/assets/c5a1a42b-708e-4781-836e-eb77c06e29c3)

Create a database called "osTicket"

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: 
MySQL Password:
Click “Install Now!”
![Screen Shot 2024-10-11 at 12 16 29 AM](https://github.com/user-attachments/assets/a2c819cf-16d4-4ba2-a0b5-530ec6882255)


![Screen Shot 2024-10-09 at 11 15 00 PM](https://github.com/user-attachments/assets/9f94e5fc-83b8-42f2-9bd9-790315d37012)


If all the steps are done correctly you will see this screen!


<br />
