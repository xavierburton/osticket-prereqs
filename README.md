<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>How To Install OsTicket Youtube Video </h2>

- https://youtu.be/pKBDk7v1zmg?si=HbDsgsbm9epaWzKT

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)


<h2>osTicket Setup/ Step By Step Pictures and Instructions. </h2>

Create an Azure Virtual Machine Windows 10, 4 vCPUs
![IMG_2596](https://github.com/user-attachments/assets/695c7717-157f-423f-9935-a2f91e5b6584)
Make sure virtual machine is running and log in with credentials through remote desktop.

Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
"Extract All" from the folder.

Next Enable Internet Information Servies(IIS) As well as CGI Through Windows Control Panel.
-Click On Uninstall of change a program, next click install windows features on or off.
-Locate IIS and Enable It. Next Expand IIS and expand world wide web services. Expand Application Development Features and check CGI and click "OK".

![IMG_2600](https://github.com/user-attachments/assets/b3df3eed-1138-4dfd-b96a-8b82679fc000)
![IMG_2602](https://github.com/user-attachments/assets/76ec9390-2660-464f-a5ef-7c0ea3a976e6)
![IMG_2599](https://github.com/user-attachments/assets/0020cf56-4734-4b61-b15b-605bce14e50e)

Next From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
![IMG_2603](https://github.com/user-attachments/assets/fb0c075e-bb62-496e-b1dd-2a2942bc30ba)
![IMG_2604](https://github.com/user-attachments/assets/ea08482a-b6a8-47d5-a4fb-671a3a32b6d2)


Instructions "Next, Agree, Next Next Close."

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
![IMG_2603](https://github.com/user-attachments/assets/32d527d0-b1be-44d7-b0ef-305a88f729ef)
![IMG_2605](https://github.com/user-attachments/assets/f226a490-fdba-43d6-a267-ede6bb8f312b)
![IMG_2606](https://github.com/user-attachments/assets/bf8930ab-731f-4a5d-b23b-a3ed4f2866fa)


Instructions "Install, Yes, Next, Close"

Next Create the directory C:\PHP
Go to C drive in files and make new folder called "PHP"
![IMG_2609](https://github.com/user-attachments/assets/3352db1f-af30-4192-917a-f58c2107f4c6)


Next From the “osTicket-Installation-Files” folder, unzip (Extract All) PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder (The folder we just created.)
![IMG_2610](https://github.com/user-attachments/assets/464f1f2f-6080-41c7-a20a-00714689118d)
![IMG_2611](https://github.com/user-attachments/assets/8451a901-5d62-4439-a7e8-f8ac0422add6)
![IMG_2612](https://github.com/user-attachments/assets/4eadd9e3-5fe6-49d0-98b1-234f656e6eb3)

Next From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
Instructions: "Agree, Install, close"
![IMG_2613](https://github.com/user-attachments/assets/9fe501d4-0b34-4ad1-8b92-5afcd3e41501)
![IMG_2615](https://github.com/user-attachments/assets/fdcdda5b-878a-4890-b43b-2c8e15b6ff9e)

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Instructions: "Next, Agree, Next, Click Typical, Install, Yes, Launch, Yes, Next, Choose Standard Configuration, Next, Next, This Part is important, Type in a rememberable password for yourself (write it down) and type into both boxes. Next, Excecute, and then Finish.

![IMG_2616](https://github.com/user-attachments/assets/bd2f4476-4c5b-4bc5-9dd3-dce855f21b39)
![IMG_2617](https://github.com/user-attachments/assets/25fcecae-5ba0-4730-9801-c9378e1e8fd8)

Next open IIS and run as an administrator 
![IMG_2618](https://github.com/user-attachments/assets/1912ca83-47f2-48db-95a6-2bd6b2257d1d)

From there Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe).
Instructions: Open PHP Manager, register new php version, click 3 dots and browse to Php folder in c drive. double click php folder and double click "php-cgi" application. click "Ok'
![IMG_2619](https://github.com/user-attachments/assets/08e86456-a1e5-4f3e-93b2-41251694cb80)
![IMG_2620](https://github.com/user-attachments/assets/60995eb1-1aa0-4014-a6aa-341eecd4a900)
![IMG_2621](https://github.com/user-attachments/assets/4b10c873-5825-484b-98a6-ce0d87005865)


After Reload IIS (Open IIS, Stop and Start the server)

Next install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, extract all “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

![IMG_2639](https://github.com/user-attachments/assets/59ad6806-6841-4877-b763-88cd21dab396)
![IMG_2642](https://github.com/user-attachments/assets/1b149dbe-a44a-416b-81fe-d55c79336d01)
![IMG_2643](https://github.com/user-attachments/assets/aceaf2d5-5e73-4bf8-97e3-e3480003cfc8)

Once the copying is complete, rename the new "upload" folder to "osTicket"
![IMG_2645](https://github.com/user-attachments/assets/5f47d857-c219-4dea-8f10-4ba578b39014)

Reload IIS (Open IIS, Stop and Start the server) once again.
![IMG_2646](https://github.com/user-attachments/assets/7b67aabb-e4a3-4eb2-b0b8-60aec128e965)




















