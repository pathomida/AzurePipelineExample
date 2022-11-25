# AzurePipelineExample
- Powershell Commands to deploy resources via ARM
    - $subscription = "0ea55d77-1224-4a86-a888-913c1ed0fb83"
    - Import-Module -Name Az
    - Connect-AzAccount #Connect to your azure account
    - Get-AzSubscription #List the all subscriptions in your account
    - Select-AzSubscription -SubscriptionId $subscription # switch to the destinated subscription
    - New-AzResourceGroup -Name arm-vscode -Location eastus # Create a new resource group in East US
    - New-AzResourceGroupDeployment -ResourceGroupName arm-vscode -TemplateFile ./ARMExample.json -TemplateParameterFile .\Parameters\ARMExample.parameters.json #Deploy the resource

# Reference
- [Azure Resource Manager](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)
- [ARM Template](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/overview)
- [ARM Template Creation via VS Code](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/quickstart-create-templates-use-visual-studio-code?tabs=CLI)
