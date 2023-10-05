## SonicWall NSv Azure Resource Manager Templates

These files are the source for the SonicWall NSv Azure Resource Manager templates.
The templates are used to deploy SonicWall NSv instances in Azure.

This branch contains the latest templates currently in use on the Azure Marketplace.

All the files (except this README) are packaged into a zip file and submitted to the Azure Partner Center for publishing to the Azure Marketplace.


## Deploying

### Marketplace deployment

Find the SonicWall NSv product in Azure Marketplace: https://azuremarketplace.microsoft.com/marketplace/apps?search=sonicwall

You cannot view/edit the template from this location. You will need the source files (this repository).
It is possible that in the future the templates in this repo could become stale against the Marketplace version. We should do our best to keep them in sync.

### ARM template deployment

For testing, you can deploy the templates directly from a public location/repository. 

1. Edit `mainTemplate.json` and change the baseurl to point to the location or repository where the templates are stored.
Do not commit this change back to the repository. This is only for testing. The baseurl used in production is provided by Microsoft.

2. Edit the Deploy to Azure links below to point to the location of `mainTemplate.json` and `createUiDefinition.json`.
Using `createUiDefinition.json` is optional. It is used to create a custom deployment experience in the Azure portal and matches the user experience in the Marketplace.


Click the "Deploy to Azure" link to load the ARM template into your Azure subscription. 

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsonicwall%2Fsonicwall-nsv-azure-templates%2Fmaster%2FmainTemplate.json)


This link deploys the mainTemplate with the UI definition file. The UI definition file is used to create a custom deployment experience in the Azure portal. This provides the closest experience to the Marketplace.

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsonicwall%2Fsonicwall-nsv-azure-templates%2Fmaster%2FmainTemplate.json/createUIDefinitionUri/https%3A%2F%2Fraw.githubusercontent.com%2Fsonicwall%2Fsonicwall-nsv-azure-templates%2Fmaster%2FcreateUiDefinition.json)