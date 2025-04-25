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


<h2>osTicket Setup/ Step By Step Pictures and Explanation. </h2>

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





