# Builds

Your application must go through a build phase before it can be deployed to an 
environment. This initial build phase is when DXP Cloud gets the Docker images 
from your CI, creates your container environment, and runs all tasks and 
build configurations specified in your image. 

To see the builds in your project, click the *Builds* tab on the top-right side 
of any environment. The builds appear in a table that contains the following 
information for each build:

-   Status: The build's status.
-   Services: The services utilized in the build.
-   Build ID: The build's ID.
-   Branch: The GitHub branch the build ran in.
-   Commit: The Git commit that triggered the build.
-   Message: The commit message.
-   Environment: The build's environment.
-   Time: When the build ran. 
-   Member: The team member who initiated the build.

To view a build's logs, click that build's *Actions* button 
(![Actions](../../images/icon-actions.png)) 
and select *View Build Logs*. You can also deploy a build via the Actions 
button. For instructions on this, see 
[Deployments](/docs/-/knowledge_base/dxp-cloud/deployments). 

![Figure 1: The Builds table lists the builds in your project.](../../images/builds.png)

