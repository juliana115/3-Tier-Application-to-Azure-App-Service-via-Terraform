# Deploying 3 Tier Application to Azure App Service via Terraform

This Project deploys a web app to Azure App Service, connecting your webfiles from from github, deploys database and it's required dependencies.

## Providers

| Name | Version |
|------|---------|
| azurerm | >= 3.6.0 |


## Requirements and Knowledge
* Git Account and Git installed on your host
* Azure Account with an active susbcription
* Azure CLI installed on your host
* Terraform installed on your host


## Usage

> If you have teraform installed, and an [Azure account](https://azure.microsoft.com/en-us/free/) and [Azure CLI install](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)

> Open your bash terminal, make a new directory 
```
mkdir <foldername>
```
<br>

> Login to Az Cli using `az login`

> Clone this project 
```
git clone https://github.com/juliana115/3-Tier-Application-to-Azure-App-Service-via-Terraform.git
```

> Run the script below
```
terraform init
terraform plan #optional
terraform apply
```

> Login to Azure and confirm all infrastructures are deployed 


## Expected Results

Name | Description
---- | -----------
`resource_group_name` | The resource group is a like a container or room to hold your resources. 
`Azure App Service `| Azure PAAS for hosting web application, in this project We deployed Linux App service for deploying a PHP simple app, Azure will project your project url.
`App Service Plan`|The name of the app service plan, for this project - Linux B1
`storage_account`| A storage account for Auditing purposes
`MSSQL Server`| Microsoft SQL Server  for the app DB
`MSSQL Database`| Microsoft SQL Database for your Webapp

<h6>Other Important Notes:<h6>

> On main.tf line 41, you can change the repo to any app you prefered to deploy instead of my locationsearch app