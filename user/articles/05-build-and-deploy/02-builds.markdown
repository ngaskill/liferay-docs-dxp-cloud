---
header-id: builds
---

# Builds

Your application must go through a build phase before it can be deployed to an 
environment. This initial build phase is when DXP Cloud gets the Docker images 
from your CI, creates your container environment, and runs all tasks and 
build configurations specified in your image. 

To see the builds in your project, click the *Builds* tab on the top-right side 
of any environment. The builds appear in a table that contains the following 
information for each build:

-   **Status:** The build's status. 
-   **Services:** The build's DXP Cloud services. 
-   **Build ID:** The build's ID. 
-   **Branch:** The build's GitHub branch. Clicking this opens the branch in 
    GitHub. 
-   **Commit:** The Git commit that triggered the build. Clicking this opens the 
    commit in GitHub. 
-   **Message:** The commit message. 
-   **Environment:** The build's environment in DXP Cloud. 
-   **Time:** When the build ran. 
-   **Member:** The team member who initiated the build. 

| **Note:** Builds are tied to the GitHub repository associated with your DXP 
| Cloud project. During the DXP Cloud onboarding process, an initial repository 
| is provisioned for your project. This initial repository is only for trial 
| purposes---you must transfer its contents to your own GitHub repository. For 
| instructions on this, see 
| [Configuring Your GitHub Repository](/docs/-/knowledge_base/dxp-cloud/configuring-your-github-repository). 

To view a build's logs, click that build's *Actions* button 
(![Actions](../../images/icon-actions.png)) 
and select *View Build Logs*. You can also deploy a build via the Actions 
button. For instructions on this, see 
[Deployments](/docs/-/knowledge_base/dxp-cloud/deployments). 

![Figure 1: The Builds table lists the builds in your project.](../../images/builds.png)

## Customizing Your Jenkinsfile

<!-- What info should we include here? -->
