# Azure Verified Modules (AVM) for CAF tfvars Migration

| Module Name | README Link | Example Usage |
|-------------|-------------|---------------|
| **avm-res-network-virtualnetwork** (Virtual Network) | [README](https://github.com/Azure/terraform-azurerm-avm-res-network-virtualnetwork/blob/main/README.md) | ```hcl
module "avm-res-network-virtualnetwork" {
  source              = "Azure/avm-res-network-virtualnetwork/azurerm"
  address_space       = ["10.0.0.0/16"]
  location            = "East US"
  name                = "myVNet"
  resource_group_name = "myResourceGroup"
  subnets = {
    "subnet1" = { name = "subnet1"; address_prefixes = ["10.0.0.0/24"] }
    "subnet2" = { name = "subnet2"; address_prefixes = ["10.0.1.0/24"] }
  }
}
``` |
| **avm-res-compute-virtualmachine** (Virtual Machine) | [README](https://github.com/Azure/terraform-azurerm-avm-res-compute-virtualmachine/blob/main/README.md) | ```hcl
module "avm-res-compute-virtualmachine" {
  source                 = "Azure/avm-res-compute-virtualmachine/azurerm"
  admin_username         = "adminUser"
  resource_group_name    = "myResourceGroup"
  location               = "East US"
  name                   = "myVM"
  virtualmachine_sku_size = "Standard_D8s_v5"
  virtualmachine_os_type  = "Linux"
}
``` |
| **avm-res-keyvault-vault** (Key Vault) | [README](https://github.com/Azure/terraform-azurerm-avm-res-keyvault-vault/blob/main/README.md) | ```hcl
module "avm-res-keyvault-vault" {
  source              = "Azure/avm-res-keyvault-vault/azurerm"
  location            = "East US"
  name                = "myKeyVault"
  resource_group_name = "myResourceGroup"
  tenant_id           = "00000000-0000-0000-0000-000000000000"
}
``` |
| **avm-res-web-hostingenvironment** (App Service Environment) | [README](https://github.com/Azure/terraform-azurerm-avm-res-web-hostingenvironment/blob/main/README.md) | ```hcl
module "avm-res-web-hostingenvironment" {
  source              = "Azure/avm-res-web-hostingenvironment/azurerm"
  name                = "myASE"
  location            = "East US"
  resource_group_name = "myResourceGroup"
  subnet_id           = azurerm_subnet.example.id
}
``` |
| **avm-res-resources-resourcegroup** (Resource Group) | [README](https://github.com/Azure/terraform-azurerm-avm-res-resources-resourcegroup/blob/main/README.md) | ```hcl
module "avm-res-resources-resourcegroup" {
  source   = "Azure/avm-res-resources-resourcegroup/azurerm"
  name     = "myResourceGroup"
  location = "East US"
}
``` |
| **avm-res-managedidentity-userassignedidentity** (Managed Identity) | [README](https://github.com/Azure/terraform-azurerm-avm-res-managedidentity-userassignedidentity/blob/main/README.md) | ```hcl
module "avm-res-managedidentity-userassignedidentity" {
  source              = "Azure/avm-res-managedidentity-userassignedidentity/azurerm"
  name                = "myIdentity"
  resource_group_name = "myResourceGroup"
  location            = "East US"
}
``` |
