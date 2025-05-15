# Azure Verified Modules (AVM) for CAF tfvars Migration

# CAF to AVM Module Mapping

| Folder Name | CAF File                   | Relevant AVM File Name         | AVM Module Name                           | AVM Module Link                                                                                 |
|-------------|----------------------------|--------------------------------|-------------------------------------------|-----------------------------------------------------------------------------------------------|
| networking  | bastion.tfvars             | bastion.tf                     | avm-res-network-bastionhost               | [Terraform Registry](https://registry.terraform.io/modules/Azure/avm-res-network-bastionhost/azurerm) |
|             | nsg_defititions.tfvars     | network_security_group.tf      | avm-res-network-networksecuritygroup       | [Terraform Registry](https://registry.terraform.io/modules/Azure/avm-res-network-networksecuritygroup/azurerm) |
|             | public_ip_addresses.tfvars | public_ip_addresses.tf         | avm-res-network-publicipaddress           | [Terraform Registry](https://registry.terraform.io/modules/Azure/avm-res-network-publicipaddress/azurerm) |
|             | virtual_networks.tfvars    | virtual_networks.tf            | avm-res-network-virtualnetwork            | [Terraform Registry](https://registry.terraform.io/modules/Azure/avm-res-network-virtualnetwork/azurerm) |
|             | configuration.tfvars       | resource_groups.tf             | avm-res-resources-resourcegroup           | [Terraform Registry](https://registry.terraform.io/modules/Azure/avm-res-resources-resourcegroup/azurerm) |
