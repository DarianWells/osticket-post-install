<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Post-Install Configuration</h1>
This tutorial outlines the post-install configuration of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Post-Install Configuration Objectives</h2>

- Configure Roles
- Configure Departments
- Configure Teams
- Setup osTicket so anyone can submit a ticket
- Create example Agents (Workers) and Users (Customers)
- Configure the SLA (Service Level Agreement)
- Create help topics

<h2>Configuration Steps</h2>

Configuring Roles

1. Go to the osTicket admin login page using this link: http://localhost/osTicket/scp/login.php . Go ahead and login using the username and password created during the installation guide.

2. Go to the admin panel by click the 'Admin Panel' button on the top of the page (you'll know you're in the admin panel when 'Agent Panel' is displayed at the top and the 'Admin Panel' button is not an option).

3. Go to the 'Agents' tab.

4. Click 'Roles'. Then select 'Add New Role'

5. Name the role "Supreme Admin" then go to the Permissions tab.

6. Check the boxes for all permissons under each of the sections under the 'Permissons' tab (Tickets, Tasks, and Knowledgebase sections). Select 'Add Role'.

7. Now Supreme Admin has been added as an available role for the osTicket system.





Configuring Departments

Departments are useful as tickets can be seprated and assigned to specific departments depending on the nature of the problem described on a ticket. Teams and agents can be assigned to a single or multiple departments in order to view tickets and streamline troubleshooting and problem resolution.

1. Go to Admin Panel -> Agents -> Departments.

2. Click 'Add New Department'.

3. Name the department 'System Administrators'.

4. For 'Manager', select yourself as a manager. For now, leave all other options on the default settings. We will make edits later.

5. Select 'Create Dept'.

6. Our first department, 'System Administrators', has been successfully added!



Configuring Teams

Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.

1. Go to Admin Panel -> Agents -> Teams

2. Click 'Add New Team'

3. 

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
