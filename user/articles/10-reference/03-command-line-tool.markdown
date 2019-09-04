---
header-id: command-line-tool
---

# Command-line Tool

Liferay Cloud's command-line interface (CLI) is a tool that helps you use and 
manage DXP Cloud. For example, you can use the CLI to perform some action on a service such as `restart`, `stop`, `deploy` and much more.

## Installing the Liferay Cloud CLI

If you use a Unix-like system such as macOS or Linux, open a terminal and run 
this command: 

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

Alternatively, you can specify the remote inline as shown in the example below: 

```shell
lcp restart -p <project-id> -s <service-id> --remote <remote-alias>
```

## Showing the Service Logs

You can use the `lcp log` command to display the service 
logs your DXP Cloud project's. Here are some common examples. 

Check the logs from all services of a given project: 

```shell
lcp log --project <projectID>
```

View the logs of a specific service in a project: 

```shell
lcp log --project <projectID> --service <serviceID>
```

View the logs of a specific project in a given interval of a time:

```shell
lcp log -p <projectId> --since "4 hours ago" --until "30 minutes ago"
```

## List Projects or Services

You can use the `lcp list` command to list projects and services. Here are some 
common examples. 

See the full list of projects and services you own or collaborate on: 

```shell
lcp list
```

List a project's services: 

```shell
lcp list --project <projectID>
```

Check a specific service in a project: 

```shell
lcp list --project <projectID> --service <serviceID>
```

## Execute Commands in a Service Container

You can also use the CLI to run commands in a service container. For example, 
this runs a command in a specific service instance: 

```shell
lcp shell --project <projectID> --service <serviceID> --instance <abc123>
```

You can also run the command in any instance of your service: 

```shell
lcp scale --project <projectID> --service <serviceID> --instance <abc123> 5
```

## Access a Service's Shell

To access a service container's shell, run this command: 

```shell
lcp shell
```

This lists all the services in the container and lets you choose which one to 
access. 

Alternatively, you can access the shell of a specific service's container by 
adding the service's project ID, service ID and container ID to the `lcp shell` command. If you do not pass any of them, the CLI will prompt you choose.

```shell
lcp shell -p <projectID> -s <serviceID> -c <containerID>
```

## All Available Commands

These are all commands available on the CLI:

| Command      | Description                                   |
| -----------  | -----------                                   |
| lcp docs     | Open DXP Cloud Docs page in your browser      |
| lcp login    | Login to DXP Cloud                            |
| lcp deploy   | Deploy a service to DXP Cloud                 |
| lcp list     | Show list of projects and services            |
| lcp log      | Show logs of project, service or container    |
| lcp restart  | Restart a service                             |
| lcp scale    | Scale a service                               |
| lcp stop     | Stop a service                                |
| lcp shell    | Open a shell to a service                     |
| lcp update   | Update DXP Cloud CLI                          |