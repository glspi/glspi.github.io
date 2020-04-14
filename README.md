# CompuNet-1 PA VM, Basic
Deploys 1 PA VM into an existing Resource Group.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fcnetpalotraining.blob.core.windows.net%2Farm-public%2Fcnet-pa1.json" rel="nofollow">
   <img src="https://aka.ms/deploytoazurebutton"/>
</a>

# CompuNet-2 PA VM, LB Sandwich
Deploys 2 PA VM into an existing Resource Group in a 'Load Balancer Sandwich'.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fcnetpalotraining.blob.core.windows.net%2Farm-public%2Fgpa-deploy.json)


# Testing
Testing

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fcnetpalotraining.blob.core.windows.net%2Farm-public%2Fgpa-deploy.json)


To Deploy via PowerShell:

1. Login
    + Connect-AzAccount

1. View subscriptions
    + Get-AzSubscription

1. Set subscription
    + Set-AzContext -SubscriptionId <ID>

1. Create Resource Group
    + New-AzResourceGroup -Location WestUS2 -Name PA-ResourceGroup-Name

1. Deploy
    + New-AzResourceGroupDeployment -ResourceGroupName PA-ResourceGroup-Name -TemplateFile .\cnet-pa1.json -TemplateParameterFile .\cnet-pa1.parameters.json


To Deploy via CloudShell:
1. Upload cnet-pa1.json and cnet-pa1.parameters.json

1. Create Resource Group
    + New-AzResourceGroup -Location WestUS2 -Name PA-ResourceGroup-Name
1. cd ~
1. Deploy
    + New-AzResourceGroupDeployment -ResourceGroupName PA-ResourceGroup-Name -TemplateFile .\cnet-pa1.json -TemplateParameterFile .\cnet-pa1.parameters.json