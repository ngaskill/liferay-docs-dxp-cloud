# First Steps

-   Git & GitHub
-   JDK 8
-   Liferay Workspace w/Project SDK & Dev Studio
-   CLI (blade, DXP Cloud's CLI, or both?)

## Git and GitHub

To use DXP Cloud, you must install Git and configure it to communicate with your 
organization's GitHub account: 

1.  If your organization doesn't have a GitHub account, create one by following 
    [these instructions](https://help.github.com/articles/signing-up-for-a-new-github-account) 
    in GitHub's documentation. 

2.  Install Git on your machine. To do so, follow 
    [these instructions](https://help.github.com/articles/set-up-git) 
    in GitHub's documentation. 

## JDK 8

Development on DXP Cloud requires JDK 8. 
<!-- 
Which JDK? Oracle, OpenJDK, etc...
-->

## Liferay Workspace
<!-- 
Is it even necessary to install Workspace separately? They already get it 
built-in with the GitHub repo. 
-->
<!-- 
Do we also require Dev Studio?
-->

You must also install Liferay's development tools, including Liferay Workspace. 
You can do this via the Liferay Project SDK Installer, which installs Liferay 
Workspace and the Liferay Dev Studio IDE. For instructions on this, see 
[Installing Liferay Workspace](/docs/7-2/reference/-/knowledge_base/r/installing-liferay-workspace). 
<!-- Linked doc is outdated. Cody is updating it with these correct steps: 

-   Select Java runtime
-   Select installation directory
-   Select whether to install command line tools (e.g., blade, bnd)
-   DXP activation key file (optional)
-   Proxy configuration (Choose *Skip proxy configuration* if not needed)
-   Click *Next* to begin installation

-->

When installation completes, the directory you chose for installation will 
contain a `liferay-workspace` folder (your Workspace), and Liferay Developer 
Studio. 

## Command-line Tool

Liferay Cloud's command-line interface (CLI) is a tool that helps you use and 
manage DXP Cloud. To use the CLI, you must first install it. 

If you use a Unix-like system such as macOS or Linux, open a terminal and run 
this command: 

```bash
curl https://cdn.liferay.cloud/cli/latest/lcp.sh -fsSL | bash
```

If you get a permissions error, try running the same command with `sudo`. 

If you use Windows, download the latest version of the 
[CLI installer](https://cdn.wedeploy.com/cli/latest/we-installer-windows-amd64.msi). 
For other systems, see the list of 
[available builds](https://dl.equinox.io/wedeploy/we/stable). 

| **Note:** To deploy services on DXP Cloud, you must have 
| [Git](https://git-scm.com/) 
| installed. 
