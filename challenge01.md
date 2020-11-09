# What the Hack: Azure Arc enabled Servers 

## Challenge 1 - Onboarding servers with Azure Arc

### Pre-requisites

* Ensure you have [activated your Azure pass using these instructions](https://www.microsoftazurepass.com/Home/HowTo).

### Introduction

[Azure Arc enabled Servers](https://docs.microsoft.com/en-us/azure/azure-arc/servers/overview) allows customers to use Azure management tools on any server running in any public cloud or on-premises environment. In order to accomplish this, a [lightweight agent](https://docs.microsoft.com/en-us/azure/azure-arc/servers/agent-overview) must be deployed onto the server. Once deployed, this agent "projects" this server as an Azure Arc resource. As an Azure resource, this server can now be managed as if it were a VM hosted natively in Azure.

In this challenge, you will need to deploy an Azure VM running Windows Server with the Hyper-V role to your Azure subscription. Next, you will create a Hyper-V VM running Windows Server 2019 within that Azure VM. You will use this Windows Server 2019 VM to emulate a non-Azure VM. 

Once deployed, you will install the Azure Arc agent on the Hyper-V VM running Windows Server 2019 server and confirm that the server is visible from the Azure portal as a resource by using [Resource Graph Explorer](https://docs.microsoft.com/en-us/azure/governance/resource-graph/first-query-portal).

### Challenge

1. Deploy an Azure VM running Windows Server 2019 with the Hyper-V role installed by using the [301-nested-vms-in-virtual-network Azure QuickStart template](https://github.com/Azure/azure-quickstart-templates/tree/master/301-nested-vms-in-virtual-network). 

2. Connect to the Azure VM by using Remote Desktop and use Hyper-V Manager to create a Windows Server 2019 VM. Use the Windows Server 2019 **VHD** file available from 
[Windows Server Evaluations](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019).

   >**Note**: You will have to modify the Network Security Group associated with the network adapter of the Azure VM deployed via the Quickstart template to allow incoming RDP connections.

3. Install the the Azure Arc machine agent onto the Windows Server 2019 Hyper-V VM you created and verify that you can see the server projected into Azure from the Azure Portal.

4. Add a tag to the server and use Resource Graph Explorer to run a query showing all resources that have that tag.

### Success Criteria

1. You have deployed a Hyper-V VM running Window Server 2019.
2. You are able to see the server in the Azure Portal as an Azure resource.
3. You are able to use Resource Graph Explorer to run a query that shows your server and any applied tags.

