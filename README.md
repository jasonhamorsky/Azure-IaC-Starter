# Azure-IaC-Starter
Azure Infrastructure-as-Code starter project using Bicep. Deploys a resource group, virtual network, subnet, and virtual machine. Part of my MSSA Cloud Administrator portfolio.
# Azure Infrastructure-as-Code Starter Project (Bicep)

Azure IaC Starter — Bicep Deployment of a Virtual Machine Environment
This project demonstrates a complete, end‑to‑end Infrastructure‑as‑Code (IaC) deployment in Microsoft Azure using Bicep and Azure CLI. It provisions a fully functional virtual machine environment, validates the deployment through both CLI and Azure Portal, and documents the entire workflow with screenshots.
This repo is designed to show real‑world IaC skills, troubleshooting ability, and clean documentation.
Resources Deployed
• 	Virtual Machine (Standard_D2s_v3)
• 	Virtual Network
• 	Subnet
• 	Network Interface
• 	Network Security Group
• 	Public IP (Standard SKU)
• 	Managed OS Disk
Technologies Used
• 	Azure Bicep
• 	Azure CLI (Cloud Shell)
• 	Azure Resource Manager (ARM)
• 	Azure Portal
• 	GitHub
Repository Structure
/Bicep
    main.bicep

/screenshots
    (All CLI + Portal screenshots)

/README.md
Deployment Instructions
1. Download the Bicep template into Cloud Shell
wget https://raw.githubusercontent.com/jasonhamorsky/Azure-IaC-Starter/main/Bicep/main.bicep -O main.bicep
2. Deploy the environment
az deployment group create \
  --resource-group iac-starter-rg \
  --template-file main.bicep \
  --parameters adminPassword="*********"
The deployment completes successfully when the CLI returns to your prompt with no errors.
Verification
All verification screenshots (CLI and Portal) are located in:
/screenshots
These include:
Azure CLI
• 	Viewing the Bicep file (cat main.bicep)
• 	Listing workspace files (ls -l)
• 	Deployment status via Azure CLI
Azure Portal
• 	Resource Group overview
• 	VM overview (size, region, status)
• 	Public IP configuration (Standard SKU)
• 	NSG inbound rules
• 	VNet + Subnet configuration
• 	Deployment history showing Succeeded
What I Learned
• 	How to deploy Azure resources using Bicep instead of ARM JSON
• 	How to troubleshoot real Azure errors:
• 	SKU availability issues
• 	Region capacity restrictions
• 	Public IP SKU limitations in restricted tenants
• 	How to validate deployments using both CLI and Portal
• 	How to document IaC projects with clarity and professionalism
Next Steps
• 	Add parameters for VM name, size, and region
• 	Deploy multiple VMs using modules
• 	Add Key Vault + Private Endpoint
• 	Automate teardown with a delete script
• 	Convert this into a reusable IaC starter template
Purpose
This project demonstrates:
• 	Hands‑on Azure experience
• 	Real troubleshooting under constraints
• 	Clean IaC practices
• 	Professional documentation
• 	A reproducible workflow that others can follow
