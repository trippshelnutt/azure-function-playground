# azure-function-playground
Quick example project to play with Azure Functions.

This project has 1 function that is coded in a class library and 1 function that is in script in Azure.

4 deployment profiles were set up locally (not checked into git):

- Package Deploy - Release
- Package Deploy - Debug
- Web Deploy - Release
- Web Deploy - Debug

Package Deploy runs in read-only mode that was not allowing another function to be added as a script. Switching to the Web Deploy allowed an additional function to be added as a script. Additionally, the WEBSITE_RUN_FROM_PACKAGE application setting needed to be changed from 1 to 0.

The Azure resources were configured automatically with the first publish:

- ASP-trippplaygroundrg-bae1
  - App Service Plan - Y1 Consumption
- tripp-playground
  - App Service
- tripp-playground
  - Application Insights
- trippplayground
  - Storage Account
