**confirm connected to subscription**

az account show -o json



**Set default resource group**

az configure --defaults group=<resource group>



**BICEP - Default location points to resource group location**

Param location string = resourceGroup().location



**Create a resource group**

az group create --name <resource group> --location 'canadacentral'





**Delete resources inside resource group**

az resource delete --resource-group MyResourceGroup --name MyVm --resource-type "Microsoft.Compute/virtualMachines"



**Delete entire resource group**

az group delete --name MyResourceGroup --yes --no-wait



**BICEP - Deploy**

az deployment group create --template-file main.bicep



**Verify deployment**

az deployment group list --output table



**BICEP - Deploy (Long)**

az deployment group create \

--template-file main.bicep \

--parameters main.parameters.dev.json \

—resource-group rg-hrappmigration