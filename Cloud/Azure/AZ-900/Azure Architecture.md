## Regions and availability zones 

Region
- A set of datacenters - each region 
- Latency defined paramater - datacenters within region are not too far from each other
- Regional low-latency network 
	- A fiber connection between data centers 

How to Choose a Region 
- Chose a region closest to your users to minimise latency 
- Some features aren't in all reguions so chose wisely 
- Price - price vary from region to region 

Each Region is Paired with another. 
If primary region fails, paired region will take over 
Only one region is updated at a time 


Availability zone 
Physical location within a region 
Each zone has its own power, boolin and networking 
part of high availability feature in Azure 
Used for protecting data from failures by replicating resources between availability zones 

## Resource groups and Azure Resource Manager 
Everything in Azure is in a resource group. 

Each resource can only exist in a single resource group 
You can add/remove resources from groups 
You can move resources between groups 
Resources from multiple regions can be in one reesource group 
You can give users access to a resource group and everything in it
Resources can interact with other resources in different resource groups 
A resource group has a location or region  as it stroes meta data about the resources in int 


Azure Resource Manager (ARM)
- Interacting with any resource on azure goes through ARM 
- Any functionality added to ARM is available to any tool 
- You can deploy, manage and monitor resources 
- Tag resources 
- Access control - control access to resources 
- Dependencies - define dependencies between resources 
- Billing 
- Consistency - the same result using different tool