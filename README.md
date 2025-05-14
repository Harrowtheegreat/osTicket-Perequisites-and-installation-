<p align="center">
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






















