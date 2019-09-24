# First Steps

To work with DXP Cloud, you must install the following on your local machine: 

-   [Git & GitHub](#git-and-github)
-   [JDK 8](#jdk-8)
-   [Command-line Tool](#command-line-tool)

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

## Command-line Tool

DXP Cloud's command-line interface (CLI) is a tool that helps you use and manage 
DXP Cloud. To use the CLI, you must first install it. 

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
