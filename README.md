
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This is an easy guide to installing a help desk ticketing system called osTicket.<br/>



<h2> Software & Technologies Used</h2>

- Windows 10 (Build 19044)
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)
- Internet Information Services (IIS)

  <h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />
<p>
  
<h3 align="center"> by creating a <em>Resource Group</em>, then proceed to create a <em>Virtual Machine</em>, making sure to select your preferred <em>Region</em> during setup .</h3>




![Screenshot 2025-04-25 185246](https://github.com/user-attachments/assets/4a23e286-bb78-48b4-bcfb-15fa8539b23f)



<h3 align="center"> During the Virtual Machine setup, choose your desired availability zone, set the Security Type to <em>Trusted launch virtual machine</em>, select the Image as <em>Windows 10 Pro, version 22H2 - x64 Gen2</em>, and configure the VM Size to <em>Standard_D2s_v3 (2 vCPUs, 8 GiB memory)</em> – $70.08/month. .</h3>


![Screenshot 2025-04-25 185515](https://github.com/user-attachments/assets/66029223-657a-4cfa-8471-67c0ea3356a9)



<h3 align="center">Created a Username and password to login into the VM</h3>



![Screenshot 2025-04-25 190748](https://github.com/user-attachments/assets/94458b16-9a82-4141-9aeb-bb08206431e4)



<h3 align="center">Open your Remote Desktop Connection app on your computer and connect to your Virtual Machine that was created in Azure.</h3>

![Screenshot 2025-04-25 191900](https://github.com/user-attachments/assets/79bdb36a-58ff-4105-8ca8-912d886bad7c)



<h3 align="center">Now we need to install / Enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS)   Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser .</h3>


![Screenshot 2025-04-25 194906](https://github.com/user-attachments/assets/91f267e7-6fa6-4d49-8e5b-8283da4f9155)

<h3 align="center"> Install PHP Manager


Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.
     </h3>

![Screenshot 2025-04-25 201308](https://github.com/user-attachments/assets/9258b6e5-519e-4233-8cae-4b1bfc91c8c3)


<h3 align="center">Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.</h3>


![Screenshot 2025-05-14 194042](https://github.com/user-attachments/assets/09d4b383-eb1e-4c19-9f04-852730ffe6d5)


<h3 align="center">CREATE DIRECTORY C:\PHP


Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from Files You Need to Download, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.</h3>

![Screenshot 2025-05-15 195353](https://github.com/user-attachments/assets/90508bcc-0177-413e-b8bd-71d4e5f2e4cc)


<h3 align="center">VC_REDIST DOWNLOAD

Download and install VC_Redist, Agree with any terms and agreements and finish installing.</h3>


![Screenshot 2025-04-25 204840](https://github.com/user-attachments/assets/870d0d24-2b84-443b-a0b8-e5442676d4fa)


<h3 align="center">DOWNLOAD MySQL
Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket.</h3>

![Screenshot 2025-04-25 205130](https://github.com/user-attachments/assets/e9d5648f-c3ea-4ab6-b11d-5aa27329af84)

![Screenshot 2025-04-25 205246](https://github.com/user-attachments/assets/288b15bd-3db8-4e53-8976-d55629a1802a)

<h3 align="center">Install osTicket v1.15.8

Download osTicket (download from within lab files: link).

Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:</h3>

![Screenshot 2025-05-15 223137](https://github.com/user-attachments/assets/e63a8274-c4de-47cd-a287-cf5df9d9399a)

![Screenshot 2025-05-15 202922](https://github.com/user-attachments/assets/d85db9f4-0377-4f51-91d4-7db744885373)

Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:

![Screenshot 2025-05-15 202959](https://github.com/user-attachments/assets/f9e9e323-e10d-47f2-9692-08fe6dda234b)


<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket:    </h3>

![Screenshot 2025-05-16 195159](https://github.com/user-attachments/assets/1093d04b-2c31-4f2f-bc23-9403a60c74d7)

On the right, click “Browse *:80”:
![Screenshot 2025-05-16 195235](https://github.com/user-attachments/assets/be586fbf-fcb4-4e9c-b5cd-7a9380107591)

<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled

Go back to IIS, sites -> Default -> osTicket.

Double-click PHP Manager:
</h3>

![Screenshot 2025-05-16 195348](https://github.com/user-attachments/assets/506176ca-4a8f-4d6b-88a6-8bbd46b1b2be)


Click “Enable or disable an extension”.

Enable: php_imap.dll.

Enable: php_intl.dll.

Enable: php_opcache.dll:

![Screenshot 2025-04-25 220250](https://github.com/user-attachments/assets/93ab4589-ba34-49fa-beb1-c64ad6b84a6b)

Refresh the osTicket site in your browser, observe the changes
![Screenshot 2025-05-16 195649](https://github.com/user-attachments/assets/1bbe9f20-6953-43f0-adbe-5c6bbfdb7112)


<h3 align="center">Rename

From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.

To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:</h3>

![Screenshot 2025-04-25 220844](https://github.com/user-attachments/assets/75aea537-8a75-4e6c-8000-73bf5d83a192)

<h3 align="center">Assign Permissions: ost-config.php

Disable inheritance -> Remove All:</h3>

![Screenshot 2025-04-25 220953](https://github.com/user-attachments/assets/db00e13e-ab95-48e6-bcad-a5e4299151f8)

New Permissions -> Everyone -> All:

![Screenshot 2025-04-25 221047](https://github.com/user-attachments/assets/18fcb453-38e3-4d57-833b-8ea31ab30bd1)
![Screenshot 2025-05-16 201842](https://github.com/user-attachments/assets/44500e63-f503-4c43-9c13-850e1146dd1c)
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)

Name Helpdesk.

Default email (receives email from customers):</h3>
![Screenshot 2025-05-16 202443](https://github.com/user-attachments/assets/a1dcb2ac-1f30-4d56-aa40-a9dfdf264bce)

![Screenshot 2025-05-16 202453](https://github.com/user-attachments/assets/e397a5cf-1c42-4f83-8206-9d1930b9dba7)

<h3 align="center">Download and Install HeidiSQL
</h3>


![Screenshot 2025-04-25 221732](https://github.com/user-attachments/assets/a96ef339-31fe-4de3-888f-3193de4fad7c)

Create a new session, root/Password1.

Connect to the session:

![Screenshot 2025-04-25 221904](https://github.com/user-attachments/assets/a2e6f6ad-fd7b-47a3-921c-0b2dd4117be9)

Create a database called “osTicket”:

![Screenshot 2025-04-25 222019](https://github.com/user-attachments/assets/2963755c-105d-4d7a-ae1b-f1e1025b9e13)

<h3 Continue Setting up osTicket in the browser

MySQL Database: osTicket

MySQL Username: root

MySQL Password: Password1:
</h3>

![Screenshot 2025-05-16 203025](https://github.com/user-attachments/assets/2e4c8a7a-db5d-45ae-8d45-cd75228e6002)

Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)

![Screenshot 2025-04-25 222507](https://github.com/user-attachments/assets/96547afb-5204-4f0b-a7b3-5ddac647adda)







