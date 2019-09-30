---
header-id: team-collaboration-access-control
---

# Team Collaboration & Access Control

Administrators can manage team members and their roles in a DXP Cloud project. 
Each environment can have unique members, and each member can have a role that 
matches their access level in that environment. It's also possible for a team 
member to have different roles in different environments. 

Here, you'll learn these topics: 

-   [Managing Team Members](#managing-team-members)
-   [Understanding Team Roles](#understanding-team-roles)

## Managing Team Members

Follow these steps to invite a user to your environment: 

1.  Click the *Team* tab in the left menu of your environment. 

2.  Enter the user's email in the *Email* field. 

3.  Use the *Role* menu to select the role to assign to the user. These roles 
    set the user's access level in the environment. For more information, see 
    [Understanding Team Roles](#understanding-team-roles). 

4.  Click *Send Invite*. 

Current and invited team members appear in the *Members* table, in separate 
tabs. You can manage team members via the *Actions* button for each, which lets 
you change the team member's role or remove the member from the team. 

![Figure 1: The Team tab shows your team members and lets you invite new ones.](../../images/invite-member.png)

![Figure 2: Use the Actions button to manage each team member.](../../images/manage-members.png)

## Understanding Team Roles

You can assign these roles to team members: 

**Admin:** Has full control over the environment and its members. They have 
exclusive permission to: 

-   Enable/disable auto scaling
-   Manually downscale a service
-   Restore from a backup
-   Change user role
-   Invite members to the environment
-   Remove members from the environment
-   Enable/disable support access
-   Delete a service

Admins also have the permissions that Contributors have. 

**Contributor:** Can handle application management and most of the development 
lifecycle, but can't manage team members or perform other Admin-exclusive 
actions. They have permission to: 

-   Start a backup
-   Change VPN settings
-   Restart a service
-   Deploy a build
-   Remove themselves from the environment

**Guest:** Has view-only access. Guests can see what's happening in the 
environment but can't perform actions or make any changes. This includes not 
having access to service features such as using shell access to run commands, 
changing/creating environment variables, or specifying custom domains. They only 
have permission to: 

-   Remove themselves from the environment
