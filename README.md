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


![Screenshot 2025-04-25 190748](https://github.com/user-attachments/assets/94458b16-9a82-4141-9aeb-bb08206431e4)






