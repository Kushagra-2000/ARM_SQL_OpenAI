# Azure Resource Deployment for Retrieval-Augmented Generation (RAG)

This repository contains an ARM template (RAG_deployment.json) to deploy all the required resources for the Retrieval-Augmented Generation (RAG) project. The template includes the deployment of Azure SQL Database, Azure OpenAI resources, and models from AI Foundry.  

## Prerequisites
Before deploying the template, ensure you have the following:

- An active Azure for Student subscription
- Permissions to create resources in the selected resource group
- Sufficient quota for Azure OpenAI resources 


## Deploy to Azure
### One click Azure deployment via Azure portal UI
Click the button below to deploy the components for RAG pipeline template to your Azure for student subscription:  

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FKushagra-2000%2FARM_SQL_OpenAI%2Frefs%2Fheads%2Fmain%2FRAG_deployment.json)

### Parameters Description
| Parameter Name  | Description | Example |
| :---------------: | :------------- | :-------: |
| serverName  | The name of the SQL server to host SQL Database.  | Sample-SQL-server
| sqlDBName  | The name of the SQL Database.  | Sample-SQL-Database
| location  | Location for SQL resources. Recommended to keep location same as default value.  | eastus2
|administratorLogin | The administrator username of the SQL server for SQL authentication.  |   |
| administratorLoginPassword  | The administrator password of the SQL server for SQL authentication. |  |   
| OpenAI_account_name  | The name of Azure OpenAI resource.  | Sample-OpenAI-resource
| OpenAI_account_location  | The location of Azure OpenAI resource. Recommended to keep location same as default value.  | eastus2
| OpenAI_chat_completion_model  | The name of recommended Azure OpenAI chat completion model. | gpt-4.1
| embedding_model	  | The name of recommended Azure OpenAI embedding model.  | text-embedding-3-small

## Firewall Configuration
**Note:** After the deployment is completed successfully, you need to configure the firewall settings for the SQL server separately to allow access from your client IP addresses.

## Troubleshooting
If you encounter any issues during deployment, check the following:

- Ensure you have sufficient quota for Azure OpenAI resources.
- Verify that all parameters are correctly specified.
- Check the deployment logs in the Azure Portal for detailed error messages.
