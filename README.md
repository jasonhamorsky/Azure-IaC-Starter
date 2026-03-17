# Azure-IaC-Starter
Azure Infrastructure-as-Code starter project using Bicep. Deploys a resource group, virtual network, subnet, and virtual machine. Part of my MSSA Cloud Administrator portfolio.
# Azure Infrastructure-as-Code Starter Project (Bicep)

Azure IaC Starter — Bicep Deployment of a Virtual Machine Environment

This project deploys a virtual machine environment in Microsoft Azure using Bicep and Azure CLI. It provisions core infrastructure components, validates the deployment through both CLI and Azure Portal, and documents the process with screenshots.

Resources Deployed
• Virtual Machine (Standard_D2s_v3)
• Virtual Network and Subnet
• Network Interface
• Network Security Group
• Public IP (Standard SKU)
• Managed OS Disk

Technologies Used
• Azure Bicep
• Azure CLI (Cloud Shell)
• Azure Resource Manager (ARM)
• Azure Portal

Repository Structure
/Bicep – main.bicep template
/screenshots – CLI and Portal validation screenshots
/README.md – deployment steps and documentation

Deployment
• Download template into Cloud Shell
• Deploy using Azure CLI:
az deployment group create --resource-group iac-starter-rg --template-file main.bicep

Verification
Deployment validated through:
• Azure CLI output and deployment status
• Azure Portal resource configuration and deployment history

Key Learnings
• Deploying Azure infrastructure using Bicep instead of ARM JSON
• Troubleshooting real deployment issues including:
– VM SKU availability
– Region capacity constraints
– Public IP SKU limitations in restricted environments
• Validating infrastructure using both CLI and Portal
• Structuring and documenting an IaC project for reproducibility

Next Steps
• Parameterize VM configuration (name, size, region)
• Use Bicep modules for reusable components
• Add Key Vault with Private Endpoint
• Implement automated teardown script
