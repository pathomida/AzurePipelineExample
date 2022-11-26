# AzurePipelineExample
- Powershell Commands to deploy resources via ARM
    - $subscription = "0ea55d77-1224-4a86-a888-913c1ed0fb83"
    - Import-Module -Name Az
    - Connect-AzAccount #Connect to your azure account
    - Get-AzSubscription #List the all subscriptions in your account
    - Select-AzSubscription -SubscriptionId $subscription # switch to the destinated subscription
    - New-AzResourceGroup -Name arm-vscode -Location eastus # Create a new resource group in East US
    - New-AzResourceGroupDeployment -ResourceGroupName arm-vscode -TemplateFile ./ARMExample.json -TemplateParameterFile .\Parameters\ARMExample.parameters.json #Deploy the resource
    - New-AzResourceGroupDeployment **-debug** -ResourceGroupName arm-vscode -TemplateFile ./ARMExample.json -TemplateParameterFile .\Parameters\ARMExample.parameters.json #Deploy the resource in Debug mode

# Reference
- [Azure Resource Manager](https://learn.microsoft.com/en-us/azure/azure-resource-manager/management/overview)
- [ARM Template](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/overview)
- [ARM Template Reference](https://learn.microsoft.com/en-us/azure/templates/)
- [ARM Template Creation Demo via VS Code](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/quickstart-create-templates-use-visual-studio-code?tabs=CLI)
- [Synapse Deployment ARM Example](https://github.com/Azure/azure-quickstart-templates/blob/master/quickstarts/microsoft.synapse/synapse-poc/azuredeploy.json)
- [Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/)
- [Azure Deployment History for troubleshooting](https://learn.microsoft.com/en-us/azure/azure-resource-manager/templates/deployment-history?tabs=azure-portal)
- [ARM Template Example](https://github.com/lordozb/github-4/blob/a83560abf1286267ce48e1bfc39ed5d1fe302287/TemplateForWorkspace.json) [2nd Example](https://github.com/nisinha/cicd/blob/a7bdf1d48c059a3ade5fe9390b89533f92939293/testrepo/ARMTemplateForWorkspace.json)
