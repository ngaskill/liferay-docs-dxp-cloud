---
header-id: command-line-tool
---

# Command-line Tool

Liferay DXP Cloud's command-line interface (CLI) is a tool that helps you use 
and manage DXP Cloud. For example, you can use the CLI to restart, stop, and 
deploy services, display logs, and more. 

-   [Installing the CLI](#installing-the-cli)
-   [Changing the CLI Remote](#changing-the-cli-remote)
-   [Showing the Service Logs](#showing-the-service-logs)
-   [List Projects or Services](#list-projects-or-services)
-   [Execute Commands in a Service Container](#execute-commands-in-a-service-container)
-   [Stop a Service](#stop-a-service)
-   [Restart a Service](#restart-a-service)
-   [Scale a Service](#scale-a-service)
-   [Access a Service's Shell](#access-a-services-shell)
-   [Available Commands](#available-commands)

## Installing the CLI

If you use a Unix-like system such as macOS or Linux, run this command in a 
terminal to instal the CLI: 

```bash
curl https://cdn.liferay.cloud/cli/install.sh -fsSL | bash
```

If you get a permissions error, try running the same command with `sudo`. 

If you use Windows, download the latest version of the 
[CLI installer](https://cdn.liferay.cloud/cli/latest/<FILE-NAME>.msi). 
For other systems, see the list of 
[available builds](https://dl.equinox.io/liferaycloud/cli/stable). 

## Changing the CLI Remote

To access DXP Cloud services via the CLI, your CLI must be pointed to the right 
DXP Cloud remote. The remote URL for DXP Cloud is `liferay.cloud`. To list the CLI's 
remotes, run this command: 

```shell
lcp remote
```

Follow these steps to change the default remote: 

1.  Add a new remote, if needed (if the remote you want to set as default 
    already exists, then you don't need to do this step): 

    ```shell
    lcp remote set <remote-alias> <remote-url>
    ```

2.  Run this command to set the default remote: 

    ```shell
    lcp remote default <remote-alias>
    ```

3.  If you need to remove a remote, run this command: 

    ```shell
    lcp remote rm <remote-alias>
    ```

Alternatively, you can specify the remote inline as shown here: 

```shell
lcp restart -p <project-id> -s <service-id> --remote <remote-alias>
```

## Showing the Service Logs

You can use the `lcp log` command to display your DXP Cloud project's service 
logs. Here are some common examples. 

See all of a project's service logs: 

```shell
lcp log --project <projectID>
```

See all of a project's service logs in a given environment:

```shell
lcp log --project <projectID> --environment <environmentID>
```

View the logs of a given service in a project: 

```shell
lcp log --project <projectID> --service <serviceID>
```

View the logs of a given service container: 

```shell
lcp log --project <projectID> --service <serviceID> --container <containerID>
```

View a project's logs from a given time interval: 

```shell
lcp log -p <projectId> --since "4 hours ago" --until "30 minutes ago"
```

View the logs of a specific project in a given interval of a time in French:

View a project's logs from a given time interval in a different language. This 
example displays the logs in French: 

```shell
lcp log --since "il y a 1 jour" --until "hier" --lang "french" -r st
```

## List Projects or Services

You can use the `lcp list` command to list projects and services. Here are some 
common examples. 

See the full list of projects and services you own or collaborate on: 

```shell
lcp list
```

See the full list of projects and services you own or collaborate on in a given 
environment: 

```shell
lcp list --environment <environmentID>
```

List a project's services: 

```shell
lcp list --project <projectID>
```

See the full list of projects and services you own or collaborate on in a given 
environment of a given remote: 

```shell
lcp list --environment <environmentID> --remote <remote-alias>
```

View a given service in a project: 

```shell
lcp list --project <projectID> --service <serviceID>
```

## Execute Commands in a Service Container

You can also use the CLI to run commands in a service container. For example, 
this runs a command in a given service instance: 

```shell
lcp shell --project <projectID> --service <serviceID> --instance <abc123>
```

You can also run the command in any instance of your service: 

```shell
lcp scale --project <projectID> --service <serviceID> --instance <abc123> 5
```

## Stop a Service

You can also use the CLI to stop a service. You can use all available flags for 
this command to specify an environment, project, or remote. 

When you run this command, the CLI prompts you to choose a service to stop from 
all available services: 

```shell
lcp stop
```

This command does the same for the services in a given project: 

```shell
lcp stop --project <projectID>
```

Alternatively, you can provide the project and service IDs to stop a given 
service: 

```shell
lcp stop --project <projectID> --service <serviceID>
```

## Restart a Service

Restarting a service from the CLI is simple. You can use all available flags for 
this command to specify an environment, project, or remote. 

When you run this command, the CLI prompts you to choose a service to restart 
from all available services: 

```shell
lcp restart
```

This command does the same for the services in a given project: 

```shell
lcp restart --project <projectID>
```

Alternatively, you can provide the project and service IDs to restart a given 
service: 

```shell
lcp restart --project <projectID> --service <serviceID>
```

## Scale a Service

To configure the number of instances for a specific service, you can run the 
`scale` command from the CLI. You can use all available flags for this command 
to specify an environment, project, service, or remote. 

When you run this command, the CLI prompts you to choose a service to scale from 
all available services: 

```shell
lcp scale
```

This command does the same for the services in a given project: 

```shell
lcp scale --project <projectID>
```

Alternatively, you can provide the project and service IDs to scale a given 
service: 

```shell
lcp scale --project <projectID> --service <serviceID>
```

## Access a Service's Shell

To access a service container's shell, run this command: 

```shell
lcp shell
```

This lists all the services in the container and lets you choose which one to 
access. 

Alternatively, you can access the shell of a specific service's container by 
passing the service's project ID, service ID, and container ID to the 
`lcp shell` command. If you do not pass any of these, the CLI prompts you 
choose. 

```shell
lcp shell -p <projectID> -s <serviceID> -c <containerID>
```

## Available Commands

These commands are available in the CLI: 

Command        | Description |
-------------- | ----------- |
`lcp docs`     | Open a DXP Cloud Docs page in your browser. |
`lcp login`    | Log in to DXP Cloud. |
`lcp deploy`   | Deploy a service to DXP Cloud. |
`lcp list`     | Show a list of projects and services. |
`lcp log`      | Show the logs of a project, service, or container. |
`lcp restart`  | Restart a service. |
`lcp scale`    | Scale a service. |
`lcp stop`     | Stop a service. |
`lcp shell`    | Open a shell to a service. |
`lcp update`   | Update the DXP Cloud CLI. |
