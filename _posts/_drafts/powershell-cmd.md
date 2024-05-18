**Log In**

**Log into Azure Tenant**

Connect-AzAccount -TenantID ‘<subscription id>’

**Set Subscription**

Set-AzAccount -Subscription ‘<subscription id>’



**RDP directly from PowerShell**

mstsc /v:<servername>



**Azure VM SSH**

- manage  SSH Keys downloaded from Azure

ssh -i /Users/lsobremonte/Downloads azureuser@40.76.32.72/logging-vm-01_key.pem 



**Subscriptions**

**Set default Subscription**

Set-Az Context -Subscription “<subscription “id>”



**Delete Resource Group**

az group delete --name <resourcegroup>



**Users**

**Get list of users within a security group**

Get-AzADGroupMember -GroupDisplayName 'License - D365 Team Members'



**Create a M365 User and Mailbox**

 New-Mailbox -Alias fourvisionSMTP -Name fourvisionSMTP -FirstName Fourvision -LastName SMTP -DisplayName "FourVision SMTP" -MicrosoftOnlineServicesID fourvisonSMTP.service@lvs1.com -Password (ConvertTo-SecureString -String 'P@ssw0rd' -AsPlainText -Force) -ResetPasswordOnNextLogon $true



**Virtual Machines**

**Get List of VMs**

 Get-AzResource -ResourceType Microsoft.Compute/virtualMachines



 **Confirm VM Disk encryption**

Get-AzVMDiskEncryptionStatus -ResourceGroupName rg_linuxVMs -VMName linux02test



**Allow PING in Windows Server**

 New-NetFirewallRule –DisplayName "Allow ICMPv4-In" –Protocol ICMPv4



**Create a Secret**

Az keyvault secret set --vault-name <vaultname> --name "AdminPassword" --value "password123"

- Assign the specific keyvault object directly to application Identity or even the VM identity (Managed Identity)

**Get List of resources**

az resource list -o table

**Get version of Azure AD Sync**

(Get-Item "C:\Program Files\Microsoft Azure Active Directory Connect\AzureADConnect.exe").VersionInfo.FileVersion

**Storage**

**Create a blob container**

azcopy make "https://waimportdemo123456.blob.core.windows.net/azcopycontainer"

**Upload to a blob container**

azcopy copy 'azcopytestdir/testfile

'https://waimportdemo123456.blob.core.windows.net/azcopycontainer'

**Passwords**

**Set Password to Never Expire for user account**

[https://docs.microsoft.com/en-us/microsoft-365/admin/add-users/set-password-to-never-expire?view=o365-worldwide](https://docs.microsoft.com/en-us/microsoft-365/admin/add-users/set-password-to-never-expire?view=o365-worldwide)

Set-AzureADUser -ObjectId odisentinel_svc@LVS.onmicrosoft.com -PasswordPolicies DisablePasswordExpiration 





**Check for expired policy for a password**

 Get-AzureADUser -ObjectId LVSAutomation_svc@lvs1.com | Select-Object UserprincipalName,@{

    N="PasswordNeverExpires";E={$_.PasswordPolicies -contains "DisablePasswordExpiration"}