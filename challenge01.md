# What the Hack: Azure Arc enabled Servers 

## Challenge 1 - Onboarding servers with Azure Arc

### Pre-requisites

* Ensure you have [activated your Azure pass using these instructions](https://www.microsoftazurepass.com/Home/HowTo).

* Download and install [Git SCM](https://git-scm.com/download) if you don't have it or a similar Git client installed

* Download and install [Visual Studio Code](https://code.visualstudio.com) if you don't already have it or a similar tool installed.

* (Optional for users with Windows devices) Have access to a local bash shell environment. There are many ways to accomplish this. We recommend considering [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10) or [Git Bash](https://gitforwindows.org/).

* (Optional) [Create an SSH key pair](https://docs.microsoft.com/en-us/azure/virtual-machines/linux/mac-create-ssh-keys)


### Introduction

[Azure Arc enabled Servers](https://docs.microsoft.com/en-us/azure/azure-arc/servers/overview) allows customers to use Azure management tools on any server running in any public cloud or on-premises environment. In order to accomplish this, a [lightweight agent](https://docs.microsoft.com/en-us/azure/azure-arc/servers/agent-overview) must be deployed onto the server. Once deployed, this agent "projects" this server as an Azure Arc resource. As an Azure resource, this server can now be managed as if it were a VM hosted natively in Azure. 

In this challenge, you will need to deploy a server to your Azure subscription. This server is deployed in Azure for the purpose of the lab, the actions you take to enable it as an Azure Arc enabled server are exactly the same if they were on-premises or in a different cloud provider. 

Once deployed, you will install the Azure Arc agent on the server and confirm that the server is visible from the Azure portal as a resource by using [Resource Graph Explorer](https://docs.microsoft.com/en-us/azure/governance/resource-graph/first-query-portal).



### Challenge

1. Deploy a server running a [supported OS](https://docs.microsoft.com/en-us/azure/azure-arc/servers/agent-overview#supported-operating-systems) to your Azure subscription. Be sure that the server you deploy has a public IP address. 

2. Install the the Azure Arc machine agent onto the server you deployed and verify that you can see the server projected into Azure from the Azure Portal.

3. Add a tag to the server and use Resource Graph Explorer to run a query showing all resources that have that tag.

### Success Criteria

1. You have deployed a server with a public IP address running in a non-Azure public cloud or on-prem environment.
2. You are able to see the server in the Azure Portal as an Azure resource.
3. You are able to use Resource Graph Explorer to run a query that shows your server and any applied tags.

