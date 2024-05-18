---

title: Quickstart - Azure CLI
description: Azure CLI quickstart guide
date: 2024-05-18 6:35:00 -0600
categories: [tools]
tags: [cmd, azure, cloud, cli]
image:
  path: /assets/images/covers/cover-terminal-icon.png
  thumbnail: /assets/images/covers/cover-terminal-icon.png
  alt: "Tools - Aliases and Shortcuts"
media_subpath: /assets/images/

---

### Login

- `az login --tenant "<tenant id>"` - login
- `az account list --output table`- get list of subscriptions
- `az account set --subscription "<subscription id>"` - set active subscription

### Confirm set subscription
- `az account show` 
- `az account show -o json` - verbose
- `az account show --query 'id' --output tsv `- shows only tenant id

### Discover
- `az find <command>` - find command usage
- `az interactive` - easy mode show next command and help info
- `az network nsg --help` - help

### Set default values
- `az init` - like setting variables makes things less cumbersome

### Users
`Get-AzADGroupMember -GroupDisplayName "<security group>"` - Get list of users within a security group

### Remove user from Management Group scope
```bash
az role assignment delete --assignee "<UPN>" --role "User Access Administrator"  --scope "/"
```

### Virtual Machines
- `az vm list `- get list of VMs
- `ssh <public ip address>` - ssh into VM

**Get IP address of VM**
```bash
az vm list-ip-addresses --resource-group $resourceGroup --name $vmname
```

## Resource Groups
- `az group list` - get list of resource groups
- `az group wait --name <resource group> --deleted` - Delete Resource Group
- `az group delete --name <resource group> --no-wait` - Delete Resource Group (Fast no wait)

### Subscription
**Get subscription tags**
```bash
az tag list --resource-id "/subscriptions/ "<subscriptionid>"
```
**Tag a subscription**
```bash
az account update --subscription <Subscription-ID> --set tags.environment=test
```
**Add subscription into management group**
```bash
az account management-group subscription add --management-group <management-group-name> --subscription <subscription-id>
```
**Deploy Subscription**
```bash
az deployment sub create_ --name demoSubDeployment --location centralus --template-file main.bicep --parameters rgName=demoResourceGroup rgLocation=canadacentral
```
