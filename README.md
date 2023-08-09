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
<img width="960" alt="1 configure roles - osticket login" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/82c9ffcc-ee3f-4caf-8c91-5a5ce423e7a2">

2. Go to the admin panel by click the 'Admin Panel' button on the top of the page (you'll know you're in the admin panel when 'Agent Panel' is displayed at the top and the 'Admin Panel' button is not an option).
<img width="960" alt="2 configure roles - os ticket login home page" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/53912e5c-4e6d-4543-876e-ac936c49299d">

3. Go to the 'Agents' tab.
<img width="960" alt="3 configure roles - admin panel" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/8d5eb2f1-47dc-4133-93d2-a98e3fea2a07">

4. Click 'Roles'. Then select 'Add New Role'
<img width="960" alt="4 configure roles - add new role" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/b67e7d0b-f894-4edf-aa31-11d0bae8be9e">

5. Name the role "Supreme Admin" then go to the Permissions tab.

6. Check the boxes for all permissons under each of the sections under the 'Permissons' tab (Tickets, Tasks, and Knowledgebase sections). Select 'Add Role'.
<img width="960" alt="5 Configure roles - supreme admin permissions" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/170fbe46-50c8-473b-bd01-a15ca956583b">

7. Now Supreme Admin has been added as an available role for the osTicket system.
<img width="960" alt="6 Configure roles - supreme admin role available" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/1fcbd878-b87b-4bbc-ba2f-c18eda019726">





Configuring Departments

Departments are necessary as tickets are routed and assigned to specific departments depending on the nature of the problem described on a ticket. Teams and agents can be assigned from a single or multiple departments in order to view tickets and streamline troubleshooting and problem resolution.

1. Go to Admin Panel -> Agents -> Departments.
<img width="960" alt="1 Departments Tab" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/2af109ca-ddb5-4c21-9dd4-a4e8c424ed1c">

2. Click 'Add New Department'.

3. Name the department 'System Administrators'.

4. For 'Manager', select yourself as a manager. For now, leave all other options on the default settings. We will make edits later.
<img width="960" alt="2 System administator settings" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/4f6b2bdb-8038-4c07-afec-cdb5351413b7">

5. Select 'Create Dept'.

6. Our first department, 'System Administrators', has been successfully added!
<img width="960" alt="3 successfully added department" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/ecbe50e0-50a3-45d4-a50f-a4c230822ed6">



Configuring Teams

Teams allow you to pull Agents from different Departments and organize them to handle a specific issue or user via a Help Topic or Ticket Filter.

1. Go to Admin Panel -> Agents -> Teams
<img width="647" alt="1 Teams tab" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/b431fdc5-8890-45fc-89fb-4a59e9fd7cbd">

2. Click 'Add New Team'
<img width="609" alt="2 add team" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/bd427983-211e-494c-8eb5-0ca3618f38bf">

3. Name the team 'Level II Support'.

4. Go to the 'Members' tab, and add yourself as a team member.
<img width="590" alt="3 add self as team member" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/d885e50e-e709-40fc-b9de-eb662a9f29d0">

5. Select 'Create Team'

6. Level II Support has been successfully added as a team!
<img width="591" alt="4 team successfully created" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/8be4f063-fb45-4204-a863-c28c77418662">


Allow so anyone can create tickets

Next, we will setup our ticketing system to allow anyone to be able to and submit a ticket, even without a user account.

1. Go to Admin Panel -> Settings -> Users

2. Uncheck the box that says 'Require registration and login to create tickets'. Then save changes.
<img width="583" alt="1 setting screen" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/13928a51-bf8a-4f9b-b5cb-74568ce2e362">


Configuring Agents (Workers)

Agents are given access to the help desk with the intent to respond and resolve the tickets. When adding an Agent to the help desk, they will need to be assigned to a Primary Department and given a Primary Role for the Tickets/Tasks routed to that department.

1. Go to Admin Panel -> Agents -> Agents

2. Click 'Add New Agent'
<img width="590" alt="1 Add new agent" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/3025bf41-1bab-4d17-87c9-6f8d1bcb4dd0">

3. Name the agent Jane Doe. for the email, use jane.doe@osticket.com.

4. Make Jane's username jane.doe.
<img width="547" alt="2 jane doe create" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/dbdfce1e-f25d-4ecf-a2ca-a1ac1454c7f9">

5. Click 'Set Password'. Uncheck 'Send the agent a password reset email' and then you will see a text field to create a password for Jane. Use Password1.

6. Uncheck 'Require password change at next login'. Set the password. 
<img width="365" alt="3 jane doe password uncheck boxes" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/ca6d7e00-65c7-44fe-a477-d6b6e167af3d">

7. Go to the 'Access' tab. Assign Jane's Primary Department to System Administrators. Select Supreme Admin as her role.
<img width="575" alt="4 jane doe dept and role" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/17069390-3592-41a0-adba-20dcbe8f81e3">

8. Go to the 'Teams' tab. Select Level II Support for her team.

9. Click 'Create'.

10. Now Jane's account has been successfully created.
<img width="569" alt="5 jane successfully created" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/61627f84-f742-4dbf-a1de-f5b818de9d03">

11. Let's create another uer. This time we'll be adding John Doe.

12. Go back to the 'Agents' section and Add New Agent.

13. We'll follow the same process as we did for creating Jane, except set John's Primary Department to Support. Set his role to View Only. Also, set Extended Access to Support.
<img width="536" alt="6 john doe" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/d6c59338-9fb9-4df0-8bad-4ef5df2de2fe">

14. Click 'Create'.

15. Now we've added both John and Jane as agents!
<img width="540" alt="7 successfully added john and jane" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/1cebe215-36c0-445a-8b56-83abaf2f66b6">


Configure Users (Customers)

Users are essentially the customers who request support from the help desk. Users are the ticket owners of the tickets in the help desk. When a ticket is created in the help desk, the user is associated with their email address in the User Directory of the help desk.

1. Go to Agent Panel -> Users

2. Click 'Add New User'
<img width="588" alt="1 add new user" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/60b43b7d-2e20-4362-b60c-68113c20b202">

3. Create two new users:
   - Karen Karen / karen@osticket.com
   - Ken Ken / ken@osticket.com
<img width="363" alt="2 create user karen karen" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/2fab06c1-fe9f-4db2-b37d-134eef07756e">

4. Select 'Add User'.

5. We've successfully created two new User accounts!


Configure the SLA (Service Level Agreement)

SLA Plans or Service Level Agreements, are unlimited in osTicket. The purpose of the SLA Plan is to provide a length of time in which the help desk Administrator expects tickets to be closed. Once created, SLA Plans can be determined for Departments, Ticket Filters, and Help Topics.

1. We'll be creating 3 new SLA Plans. Go to Admin Panel -> Manage -> SLA

2. Click 'Add New SLA Plan'.
<img width="560" alt="1 Add SLA Plan" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/ddb9313a-2b91-4686-9a03-8bb18f312bfe">

3. Name the first plan SEV-A. Set the Grace Period to 1 hour. Set the Schedule to 24/7. Click 'Add Plan'. Create the next two plans by following the same steps:
   - SEV-B (4 hours, 24/7)
   - SEV-C (8 hours, business hours)
<img width="539" alt="2 SEV-A" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/823e9cb0-899b-41ce-bd1c-994f5826270b">
<img width="537" alt="3 SEV-B" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/6cecd39f-c2f8-4ef5-a13d-867d2d1e9aba">
<img width="536" alt="SEV-C" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/4e0140ca-c200-429c-80d1-ed9228184a9b">

4. Now we've finished with creating our SLA Plans.


Configure Help Topics

Help Topics will help streamline your end-user’s help desk experience to ensure proper assignment and prompt response to the ticket. Help Topics will determine what Department the ticket is routed to which will determine which Agents have access to the ticket. The Help Topic also can determine other configurations of the ticket, such as the ticket’s SLA (or Service Level Agreement) and priority of a ticket, i.e. Emergency to Low.

1. Go to Admin Panel -> Manage -> Help Topics

2. Click 'Add New Help Topic'
<img width="539" alt="1 help topics menu" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/63d3882d-2781-426a-8a40-92ae9cbd7067">

3. Name the first Help Topic 'Business Critical Outage'. Click 'Add Topic'.

4. Follow suite and create three more help topics:
   - Personal Computer Issues
   - Equipment Request
   - Password Reset

5. We've now finished with creating our different Help Topics!
<img width="539" alt="2 help topics created" src="https://github.com/DarianWells/osticket-post-install/assets/132870202/def1ec58-6f3b-4819-8503-50b6f7b97514">


That concludes the post-installation configuring for our osTicket system. We'll be using our new configurations to create tickets and observe the ticketing life-cycle in our Help Desk system.
