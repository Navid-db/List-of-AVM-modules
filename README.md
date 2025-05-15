Azure Verified Modules (AVM) Modules for CAF tfvars Migration
Module Name	README Link	Example Usage
avm-res-network-virtualnetwork (Virtual Network)	README	<pre><code>module "avm-res-network-virtualnetwork" {
source = "Azure/avm-res-network-virtualnetwork/azurerm"		
address_space = ["10.0.0.0/16"]		
location = "East US"		
name = "myVNet"		
resource_group_name = "myResourceGroup"		
subnets = {		

ini
Copy
Edit
"subnet1" = { name = "subnet1"; address_prefixes = ["10.0.0.0/24"] }
"subnet2" = { name = "subnet2"; address_prefixes = ["10.0.1.0/24"] }
}
}</code></pre>
github.com
 |
| avm-res-compute-virtualmachine (Virtual Machine) | README | <pre><code>module "avm-res-compute-virtualmachine" {
source = "Azure/avm-res-compute-virtualmachine/azurerm"
admin_username = "adminUser"
resource_group_name = "myResourceGroup"
location = "East US"
name = "myVM"
virtualmachine_sku_size = "Standard_D8s_v5"
virtualmachine_os_type = "Linux"
}</code></pre>
github.com
github.com
 |
| avm-res-keyvault-vault (Key Vault) | README | <pre><code>module "avm-res-keyvault-vault" {
source = "Azure/avm-res-keyvault-vault/azurerm"
location = "East US"
name = "myKeyVault"
resource_group_name = "myResourceGroup"
tenant_id = "00000000-0000-0000-0000-000000000000"
}</code></pre>
github.com
 |
| avm-res-web-hostingenvironment (App Service Environment) | README | <pre><code>module "avm-res-web-hostingenvironment" {
source = "Azure/avm-res-web-hostingenvironment/azurerm"
name = "myASE"
location = "East US"
resource_group_name = "myResourceGroup"
subnet_id = azurerm_subnet.example.id
}</code></pre> |
| avm-res-resources-resourcegroup (Resource Group) | README | <pre><code>module "avm-res-resources-resourcegroup" {
source = "Azure/avm-res-resources-resourcegroup/azurerm"
name = "myResourceGroup"
location = "East US"
}</code></pre>
github.com
 |
| avm-res-managedidentity-userassignedidentity (Managed Identity) | README | <pre><code>module "avm-res-managedidentity-userassignedidentity" {
source = "Azure/avm-res-managedidentity-userassignedidentity/azurerm"
name = "myIdentity"
resource_group_name = "myResourceGroup"
location = "East US"
}</code></pre>
github.com
 | Each example module block above is taken from the official module’s README and shows the required arguments for deploying the respective resource. For instance, the Virtual Network module requires address_space, location, name, and subnets (among others)
github.com
, while the Key Vault module requires location, name, resource_group_name, and tenant_id
github.com
. These Azure Verified Modules are intended to replace older CAF tfvars-based modules for these resource types. Sources: Official Azure Terraform Verified Module READMEs as linked above
