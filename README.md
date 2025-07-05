# osTicket Part 2: Create Departments, Roles, Agents, Users, Service Level Agreement (SLA), and Manage Ticketing Lifecycle

---

## Introduction

This is the second part of our exploration of the web-based ticketing system, osTicket. Completing the [first part](link-to-part-1-if-available) is a prerequisite to participating in this second part.

---

### What you will learn:

* Creating Departments and Roles
* Creating Agents and Teams
* Creating Help Topics, SLAs, and Users
* Managing Ticketing Lifecycle

---

## A Quick Refresh

In the first part of the osTicket exercise, we launched a virtual machine on the Azure portal and successfully deployed the web-based osTicket application. We then created an **Admin account** that we will use to access the osTicket platform (Helpdesk).

---

## Creating Departments and Roles

You can view **Departments** as containers that allow you to organize **Agents**. **Roles** are permissions that define what action an Agent can carry out.

Log in as admin using the link above and type your username or email, and password.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*-braFKRyxMOB1iPjbLQYog.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />


Ensure you are in the **Admin panel**. If the top-right menu bar says “Agent Panel,” you are in the “Admin panel.” You can toggle the same option to switch to “Agent Panel” as needed.

---
<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*okDBCgYHdrX3oCxgsd7Y5w.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

### Steps for Creating Departments

1.  Select the **"Agents"** tab under the **"Admin Panel"** > **Departments** > **Add New Department**.
2.  **Name**: System Administrators
3.  Select **Create Department**.

---
<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*mJQIK7z85A51ZKdH2fAarQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

### Steps for Creating Roles

1.  Select the **"Agents"** tab > **Roles** > **Add New Role**.
2.  **Name**: GlobalAdminAccess
3.  Select the **"Permissions"** tab and check every box under the **"Tickets," "Tasks,"** and **"Knowledgebase"** sections. This gives full control to the Agent that will assume the role.
4.  Select **Add Role**.

---
<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*IordCgw0I_mIfJEp2LmJSw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

## Creating Agents and Teams

**Agents** are individuals with permission to respond to and resolve tickets. **Teams** allow you to pull Agents from different Departments and organize them to handle a specific issue.

---

### Steps for Creating Agents

1.  Select the **Agent** tab > **Add New Agents**.
2.  **Name**: Pat Henshaw
3.  **Email**: phenshaw@helpesk.com
4.  **Username**: phenshaw
5.  Click **Set Password** > Uncheck the box **"Send the Agent a Password Reset Email"**.
6.  Create a password for the Agent.
7.  Uncheck **"Require Password Change at Next Login"** // *Don’t do this in the real world!*
8.  Select **"set"**.
9.  Select the **Access** tab > Select the **Department** dropdown menu > **System Administrators**.
10. Select the **Role** dropdown menu > **GlobalAdminAccess**.
11. **Extended Access** > Select **Department** > **Support** > **Add** > **GlobalAdminAccess**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*gsfHwwhYtGBGIQo8pP8deA.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

Follow the same steps to create another Agent named **“Jerry Moore”** with the details in the screenshot below.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*Y08Ro_G-YJNC3Ddn4P4ftg.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />


---

Here is a table showing all the agents:

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*Cn7aDrS-AkCrAoU2DfAq8A.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />


---

### Steps for Creating Teams

1.  Select the **"Agents"** tab > **Teams** > **Add New Team**.
2.  **Name**: Level II Support // Since we already have a default Level I support
3.  Navigate to the **"Members"** tab and select **Pat Henshaw** and your **Admin account** in the **"Select Agent"** dropdown menu.
4.  Select **Create Team**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*R_x_GKYndy2hUE19xxbjVQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

Navigate to the **Teams** tab > double-click on the default **Level I Support** team and add **Jerry Moore** as a member.

---
<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*UFuiyZgk3Da9xLFIRUCTHg.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

## Creating Help Topics, SLAs, and Users

**Help Topics** are simple captions for categorizing issues. **Users** are ticket owners. **Service Level Agreement (SLA)** is the expected time (in hours) in which an opened ticket is expected to be closed. If tickets are not closed within the stipulated time, they are considered overdue.

---

### Steps for Creating Help Topics

1.  Select the **Manage** tab > **Help Topics** > **Add New Help Topic**.
2.  **Topic**: Business Critical failure

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*Dbgg8ZKO1rmwPnZmh1r2-g.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

Follow the same steps to create some more topics like the ones below:

* Personal Computer Issues
* Password Reset

---
<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*ClqRg2ehB-cL0bWJB3TVDA.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

### Steps for Creating SLAs

1.  Select the **Manage** tab > **SLA** > **Add New SLA Plan**.
2.  **Name**: Priority 1
3.  **Grace Period**: 1
4.  **Schedule** dropdown menu: 24/7
5.  Select **Add Plan**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*hDddgb8-MJTZy2JP01V23w.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

Repeat the same steps to create SLAs with **Priorities 2 and 3**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*q5v-J_uZ_rhs-5Om4SNSHw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*OyO-s4q7nZ5yqlFmzfEHoQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

### Steps for Creating Users

1.  Ensure you are in the **Agent Panel** by toggling the **"Agent Panel"** tab.
2.  Select the **Users** tab > **Add New User**.
3.  **Email Address**: hjones@helpdesk.com
4.  **Full Name**: Henry Jones
5.  Select **Add User**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*F7clPl3U9gohzDpZIt85Ow.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

Repeat the same steps to create 2 more users as shown in the User Directory below:

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*UFCIf-8WcN9ApEwREQYljA.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

### Allow Anyone to Create Tickets:

1.  Select **Settings** > **User Settings**.
2.  Ensure to **uncheck** the box that says: **Registration Required: Require registration and login to create tickets**.

---

## Managing Ticketing Lifecycle Stages

A ticket may go through different stages in its lifecycle. The status can be set and updated either manually by an agent or automatically based on business rules. Here are the stages we will demonstrate in this exercise:

* **New**—Creating a Ticket
* **Open**—Assignment and Communication
* **Working on the issue**
* **Solved**—Resolution
* **Closed**—Automated

---

### New—Creating a Ticket

Depending on the setting of your Helpdesk, newly created tickets can be set to open manually by an agent or automatically set to open (in our case). You will create 3 tickets using the information for the 3 users you created previously.

---

#### Steps for Creating a New Ticket

1.  Navigate to `http://localhost/osticket`.
2.  Select **Open a New Ticket**.
3.  **Email Address**: hjones@helpdesk.com
4.  **Name**: Henry Jones
5.  **Help Topic** Dropdown Menu: Business Critical failure
6.  **Issue Summary**: E-commerce Website Down
7.  **Details**: Users reported items not displaying when they initiate a search on the shopping panel.
8.  **Create Ticket**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*ebzPy211r6Nrk6in4eQXag.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />


Repeat the same steps to create 2 more tickets for the remaining 2 users, using the details in the screenshot below:

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*N4vNx1K14FgZRpmPAeXGiA.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*GNebPrjUnBcIIT_trbwNiw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

### Open—Assignment and Communication

1.  Log in as Admin.
2.  Navigate to `http://localhost/osticket/scp` and log in using the credentials of an Agent in the System Administration department. We will use Pat Henshaw’s.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*-rponXbh6m-qSSNRBTiOUQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

Once you are logged in, toggle the panel to **“Agent Panel”** > **Open** > You should see all the open tickets as an Admin.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*mXBy66mVp_j1_I4_PPaw_Q.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />


---

#### Assign the Most Critical Ticket

1.  At a glance, we can tell that there’s a ticket involving critical infrastructure and we have to give priority to it.
2.  Double-click on **ticket #218301** with the subject name **“E-commerce website down”** and update it as follows:
    * **Priority**: Emergency.
    * **Assigned to**: Pat Henshaw // A Level II Support Team member in the Sys. Admin. Department.
    * **SLA Plan**: Priority 1 // Highest priority—for business revenue impacting reasons.
    * **Department**: System Administrator // Responsible for critical business infrastructure.
    * **Response text box**: Ticket transferred to the Sys. Admin Dept, liaising with Admins to resolve issues.
3.  Select **Post Reply**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*-FxCU-Xd6UD3h9gh_MMOuw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

#### Assign Others based on relative importance

Repeat the same steps to update the other two tickets as shown below:

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*d3afk7q2PwIH-SrsHL6_Qw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*GDUNsQhtwqXdxCQkERvdBQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

### Working on the issue

#### E-commerce Website Issue:

* Agent works with the System Administration team (both Network and Database Administrators).
* They determine the root cause and take necessary action to resolve the failure.

#### Password reset issue assigned to self:

* Admin goes to the Active Directory.
* Carries out a password reset.
* Configures it to require the user to reset the password on the first login attempt.

#### PC issue assigned to Jerry Moore in the Support Dept:

* He logs in and checks tickets assigned to him.
* Communicates with the user to let them know he is working to resolve the ticket.
* Queries the user’s computer to see if they have multiple programs running. He also checks for large files in the recycle bin or temporary files of no significance.
* Closes multiple programs (if any) and deletes large and insignificant files to free up storage space.

---

### Solved—Resolution

Once the issues are resolved, the agents head back to the ticket and update the end users.

---

#### E-commerce Website Resolved:

* **Response text box**: The Database team found that the primary Db failed, so they promoted the secondary (standby) Db to handle queries from users.
* **Ticket Status**: Resolved
* Select **Post Reply**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*K-HZCCVVQ4wT6FsSsIHVeg.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

#### Password Reset Issue Resolved

* **Response text box**: Password reset carried out, user is required to reset the password on the first login attempt.
* **Ticket Status**: Resolved
* Select **Post Reply**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*dbh1j0prV_LGyThy8fy6mw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

#### Slow PC Resolved

* **Response text box**: Multiple programs running on the user’s computer have been closed and large files deleted to free up space. The user’s computer now performs optimally.
* **Ticket Status**: Resolved
* Select **Post Reply**.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*_N7jzIoCX4oP1u8z-RUjRQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

---

### Closed—Automated

Once the ticket status is set to **“Resolved”** and posted, they automatically display as closed tickets.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*2bnI0qkVgByM4-LCWSf7cQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />


---

## Conclusion

Quite a lot accomplished! You created Departments, Agents, SLAs, Help Topics, and Users. You went on to manage the lifecycle of a ticket from creating new tickets to closing them, bearing in mind the relative urgency and priorities of different tickets.

Congratulations! Feel free to check out other posts by me on Active Directory, Office (Microsoft) 365, and more. See you in the next exercise.
