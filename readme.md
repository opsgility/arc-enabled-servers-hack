# What The Hack - Azure Arc enabled Servers Hack

## Introduction

 ![](./img/image1.png)
 [Azure Arc enabled Servers](https://docs.microsoft.com/en-us/azure/azure-arc/servers/overview) allows customers to use Azure management tools on any server running in any public cloud or on-premises environment. In this hack, you will be working on a set of progressive challenges to showcase the core features of Azure Arc. 
 
 In the first challenge, you will set up your lab environment and deploy servers as VMs in a Windows Server Hyper-V host running in an Azure VM. Then, you will use Azure Arc to project these servers into Azure, and begin to enable Azure management and security tools on these servers. On successive challenges, you will apply [Azure Policy](https://docs.microsoft.com/en-us/azure/governance/policy/overview) and enable other Azure services like [Azure Security Center](https://docs.microsoft.com/en-us/azure/security-center/) on your projected workloads.

   >**Note**: Keep in mind that even though the servers you are deploying are running in an Azure VM, they are actually not Azure VMs. Instead, they are nested VMs within a Hyper-V host implemented as an Azure VM. This will allow you to configure them as Arc enabled servers. The process of configuring them throughout all challenges is practically identical to the one you would follow if you deployed servers in an on-premises datacenter or in environment hosted by a third-party public or private cloud provider. 

## Learning Objectives

This hack will help you learn:

1. Azure Arc enabled Servers basic technical usage
2. How Azure Arc enabled Servers works with other Azure services
3. How Azure Arc enabled Servers enables Azure to act as a management plane for any workload in any public or hybrid cloud

## Challenges
 - [Challenge 1](challenge01.md) - Onboarding servers with Azure Arc
 - [Challenge 2](challenge02.md) - Policy for Azure Arc connected servers
 - [Challenge 3](challenge03.md) - Arc Value Add: Integrate Security Center
 - [Challenge 4](challenge04.md) - Arc Value Add: Enable Sentinel
 - [Challenge 5](challenge05.md) - Arc Value Add: Azure Lighthouse 
 

## Prerequisites
- [Activated Azure Pass](https://www.microsoftazurepass.com/Home/HowTo)


## Contributors
- Dale Kirby
- Lior Kamrat
- Ali Hussain
