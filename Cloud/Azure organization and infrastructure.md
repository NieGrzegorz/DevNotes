
## What is Azure? 
MS **public** cloud computing platform
Over 200 products and services 
Iaas, PaaS, SaaS solutions 
Allows to supplement or replace existing on-premises computing services

Pay-as-you-go pricing - pay for what you use/consume 
User is billed by a second of using a server (called operational expense)

## Azure Global Infrastructure 
Region - Group of datacenters in single geographic location (Central US)
Availability zone - one of several unique locations in a region (One or more infividaual datacenters in a regiion)

Single region is composed of multiple datacenters and availability zones 

Region - high availability and fault tolerance  - be closer to your users, defend against regional outage 

Availability zone - fault tolerance - deploy resources across zones. Protect against single point of failure 


## Azure Services 
Over 200 services 
Azure resource management (ARM) - centralized management layer 

## Resource hierarchy and organization 


## Identity and Access Management  (IAM)

***Who can do what on which resources?***

**Who** - Azure Active Directory - Manages who is who and what 
**Can do what** - Azure Role-Based Access Control- Provide different levels of access to users 
**On which resources** - Scope - controls resources controled 

### Azure Active Directory 
Cloud-based identity service - single instance per Tenant (company)
Provides identity 
Identity - security principal 
Identities may be users or event applications 
Email format 

### Azure Role-Based Access Control (Azure RBAC)
Control access using roles 
 - What are you allowed to do
 - Assign roles to a security principal 
 - Roles are connections of specific permitions 
 - General and specific role types: 
	 - Owner - full access to all resources in a scoe
	 - Virtual Machine Contributor - only access to manage VMs


### Scope 
The set of resources allowed to access
- On which resources 
- Roles granted to various layers of resource hierarchy 
- Lower levels inherit roles from higher levels 
	- Centralized management

## Monitoring your Azure Environment 

Azure Monitor 
- Logs - text base records of events 
	- Activity logs  " Who created a resource and when"
	- OS logs 
- Metrics 
	- Telemetry-based performance data
		- CPU utilization