<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
<p> This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket. <p/>
 This is a continuation of the https://github.com/edgararturocastrejon/osticket-prereqs project. 


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Microsoft Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles (for grouping permissions)
- Configure Departments (Ticket Visibility, Help Desk vs SysAdmins, vs Networking)
- Configure Teams
- Allow anyone to create tickets
- Configure Agents (workers)
- Configure Users (customers)
- Configure SLA
- Configure Help Topics (For when users create a ticket)

<h2>Configuration Steps</h2>

<p>
 
![Screen Shot 2024-10-05 at 9 45 10 AM](https://github.com/user-attachments/assets/b6f5b1ae-386d-42da-bca5-62a7775a35bd)
![Screen Shot 2024-10-05 at 9 58 19 AM](https://github.com/user-attachments/assets/d0de9add-3631-4e96-806f-871b60f1c56b)

</p>
<p>
1) Login to the Admin/Analyst login page: http://localhost/osTicket/scp/login.php in the Virtual Machine VM) </p>
Acknowledge Agent Panel vs Admin Panel on the top right corner
</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 02 30 AM](https://github.com/user-attachments/assets/316393d7-989b-408d-8d91-17332664ec10)
![Screen Shot 2024-10-05 at 10 02 34 AM](https://github.com/user-attachments/assets/81892237-f61c-446f-bfb0-749852b3b398)
![Screen Shot 2024-10-05 at 10 03 29 AM](https://github.com/user-attachments/assets/e32ecf37-ab67-4b2b-af31-ab1eb5c2a72a)

</p>
<p>
Configure Roles (for grouping permissions) <p/>
Admin Panel -> Agents -> Roles <p/>
Give Supreme complete access under "Permissions" check all the check marks in "Tickets" "Task" and "knowledgebase"
</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 13 48 AM](https://github.com/user-attachments/assets/3ab886f2-07c1-43e6-922e-e83dc776fb7a)
![Screen Shot 2024-10-05 at 10 13 59 AM](https://github.com/user-attachments/assets/5272e7e3-7e39-4dcc-93e0-88efa6d6b358)

</p>
<p>
Configure Departments <p/> 
Admin Panel -> Agents -> Departments
</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 19 29 AM](https://github.com/user-attachments/assets/5aa2551f-8acb-44db-aeb5-603091f23acf)

</p>
<p> Configure Teams <p/>
Admin Panel -> Agents -> Teams (Pull Agents from different Departments)
</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 25 25 AM](https://github.com/user-attachments/assets/be007544-93d2-4552-8f92-7cf22eac9403)

</p>
<p>
Allow anyone to create tickets <p/>
Admin Panel -> Settings -> User Settings (UNCHECK: unregistered users can create tickets) <p/>
Registration Required: Require registration and login to create tickets 
</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 32 00 AM](https://github.com/user-attachments/assets/202b2a4c-c7e1-44f5-ba56-590141cced7f)
![Screen Shot 2024-10-05 at 10 41 15 AM](https://github.com/user-attachments/assets/95b3e5cd-b43c-4d2a-8584-5c80be661fea)
![Screen Shot 2024-10-05 at 10 37 49 AM](https://github.com/user-attachments/assets/567a9331-b18c-4f5b-8deb-cf57cbe4111a)
![Screen Shot 2024-10-05 at 10 42 55 AM](https://github.com/user-attachments/assets/6164c3d8-38c3-477e-8802-5a618b5b8143)

</p>
<p>
Configure Agents (workers) <p/>
Admin Panel -> Agents -> Add New <p/>
Jane (Dept: SysAdmins) <p/>
John (Dept: Support)

</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 47 42 AM](https://github.com/user-attachments/assets/a317d6f0-9f2d-4fc4-b62b-2c123334313d)
![Screen Shot 2024-10-05 at 10 51 07 AM](https://github.com/user-attachments/assets/342a259a-8424-40c6-857c-09c78a8018de)

</p>
<p>
Configure Users (customers) In Agent Panel! <p/>
Agent Panel -> Users -> Add New <p/>
Karen <p/>
Ken

</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 10 57 17 AM](https://github.com/user-attachments/assets/ee948435-847b-4564-943b-e6ae09bce1ea)
![Screen Shot 2024-10-05 at 10 57 44 AM](https://github.com/user-attachments/assets/52d01cf9-77db-442b-8900-8390ca755629)
![Screen Shot 2024-10-05 at 10 58 12 AM](https://github.com/user-attachments/assets/61d667f3-c04e-4696-8ac5-2f526b5ae92e)

</p>
<p>
Configure SLA (Go back to Admin Panel) <p/>
Admin Panel -> Manage -> SLA <p/>
Sev-A (Grace Period: 1 hour, Schedule: 24/7) <p/>
Sev-B (Grace Period: 4 hours, Schedule: 24/7) <p/>
Sev-C (Grace Period: 8 hours, Business Hours)

</p>
<br />

<p>
 
![Screen Shot 2024-10-05 at 11 03 50 AM](https://github.com/user-attachments/assets/586faba4-73af-4d5d-b6b2-b27ef0b5f84e)
![Screen Shot 2024-10-05 at 12 23 16 PM](https://github.com/user-attachments/assets/dd5a38fc-178e-457a-9a9c-f95971a846ce)
![Screen Shot 2024-10-05 at 12 24 18 PM](https://github.com/user-attachments/assets/d17b7bc8-f596-4451-a3b8-b7a752ddcc9f)
![Screen Shot 2024-10-05 at 12 25 20 PM](https://github.com/user-attachments/assets/3b7cc004-0aca-4db2-a64f-797778aea514)
![Screen Shot 2024-10-05 at 12 26 01 PM](https://github.com/user-attachments/assets/ec96ae61-bafa-4570-a5cd-45de670d26ed)

</p>
<p>
Configure Help Topics (For when users create a ticket) <p/>
Admin Panel -> Manage -> Help Topics <p/>
Business Critical Outage <p/>
Personal Computer Issues <p/>
Equipment Request <p/>
Password Reset <p/>
Other
</p>
<br />
