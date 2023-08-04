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
- Configure Agents (Workers)
- Configure Users (Customers)
- Configure the SLA (Service Level Agreement)
- Create help topics

<h2>Configuration Steps</h2>

Configuring Roles

Roles are the permissions granted to Agents per Department that they have access to. Each Role has a set of permissions that can be checked/unchecked for agents given that Role in association with a Department they have access to. An unlimited number of roles can be created and assigned to Agents with access to various departments.

1. Go to the osTicket admin login page using this link: http://localhost/osTicket/scp/login.php . Go ahead and login using the username and password created during the installation guide.

2. Go to the admin panel by click the 'Admin Panel' button on the top of the page (you'll know you're in the admin panel when 'Agent Panel' is displayed at the top and the 'Admin Panel' button is not an option).

3. Go to the 'Agents' tab.

4. Click 'Roles'. Then select 'Add New Role'

5. Name the role "Supreme Admin" then go to the Permissions tab.

6. Check the boxes for all permissons under each of the sections under the 'Permissons' tab (Tickets, Tasks, and Knowledgebase sections). Select 'Add Role'.

7. Now Supreme Admin has been added as an available role for the osTicket system.





Configuring Departments

Departments are necessary as tickets are routed and assigned to specific departments depending on the nature of the problem described on a ticket. Teams and agents can be assigned from a single or multiple departments in order to view tickets and streamline troubleshooting and problem resolution.

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

3. Name the team 'Level II Support'.

4. Go to the 'Members' tab, and add yourself as a team member.

5. Select 'Create Team'

6. Level II Support has been successfully added as a team!


Allow so anyone can create tickets

Next, we will setup our ticketing system to allow anyone to be able to and submit a ticket, even without a user account.

1. Go to Admin Panel -> Settings -> Users

2. Uncheck the box that says 'Require registration and login to create tickets'. Then save changes.


Configuring Agents (Workers)

Agents are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department.

1. Go to Admin Panel -> Agents -> Agents

2. Click 'Add New Agent'

3. Name the agent Jane Doe. for the email, use jane.doe@osticket.com.

4. Make Jane's username jane.doe.

5. Click 'Set Password'. Uncheck 'Send the agent a password reset email' and then you will see a text field to create a password for Jane. Use Password1.

6. Uncheck 'Require password change at next login'. Set the password. 

7. Go to the 'Access' tab. Assign Jane's Primary Department to System Administrators. Select Supreme Admin as her role.

8. Go to the 'Teams' tab. Select Level II Support for her team.

9. Click 'Create'.

10. Now Jane's account has been successfully created.

11. Let's create another uer. This time we'll be adding John Doe.

12. Go back to the 'Agents' section and Add New Agent.

13. We'll follow the same process as we did for creating Jane, except set John's Primary Department to Support. Set his role to View Only. Also, set Extended Access to Support.

14. Click 'Create'.

15. Now we've added both John and Jane as agents!


Configure Users (Customers)

Users are essentially the customers who request support from the help desk. Users are the ticket owners of the tickets in the help desk. When a ticket is created in the help desk, the user is associated with their email address in the User Directory of the help desk.

1. Go to Agent Panel -> Users

2. Click 'Add New User'

3. Create two new users:
   - Karen Karen / karen@osticket.com
   - Ken Ken / ken@osticket.com

4. Select 'Add User'.

5. We've successfully created two new User accounts!


Configure the SLA (Service Level Agreement)

SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed. Once created, SLA Plans can be determined for Departments, Ticket Filters, and Help Topics.

1. We'll be creating 3 new SLA Plans. Go to Admin Panel -> Manage -> SLA

2. Click 'Add New SLA Plan'.

3. Name the first plan SEV-A. Set the Grace Period to 1 hour. Set the Schedule to 24/7. Click 'Add Plan'. Create the next two plans by following the same steps:
   - SEV-B (4 hours, 24/7)
   - SEV-C (8 hours, business hours)

4. Now we've finished with creating our SLA Plans.


Configure Help Topics

Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket. Help Topics will determine what Department the ticket is routed to which will determine which Agents have access to the ticket. The Help Topic also can determine other configurations of the ticket, such as the ticket’s SLA (or Service Level Agreement) and priority of a ticket, i.e. Emergency to Low.

1. Go to Admin Panel -> Manage -> Help Topics

2. Click 'Add New Help Topic'

3. Name the first Help Topic 'Business Critical Outage'. Click 'Add Topic'.

4. Follow suite and create three more help topics:
   - Personal Computer Issues
   - Equipment Request
   - Password Reset

5. We've now finished with creating our different Help Topics!


That concludes the post-installation configuring for our osTicket system. We'll be using our new configurations to create tickets and observe the ticketing life-cycle in our Help Desk system.


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
