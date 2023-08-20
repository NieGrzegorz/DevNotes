## Virtual Machines 
VMs are part of infrastructure as a service. 

Why to use VMS insdear Managed Services? 
- Flexibility 
	- Trade-off - flexiblility vs less management 


Avaliablility set - automaticatic replication of VM over different avaliability zones 
IF VM goes down, a copied VM can take over 

Scale sets 
- Multiple copies of VMs 
- Goes with load balancer 
- Scaling copies of application 
- Enables scaling and elasticity 

## Networking 
How are VMs and services communicate with outide world 

Virtual Network (VNet) - Fundamental Building Blick 
- Provides private and public network communication among Azure resources 
- Uses familiar network concepts in virtual format (subnets, firewalls, routes )
- Virual format - Software Defined Networking 
- Enables public access or extende private networking to other networks 



## Storage
All purpose stroage sollutuin for multiple data storage scenarios 
Scalable 
Managed infrastructure 
Flexible access options 
Types: 
 - Blob
	 - Object storage 
	 - Binary Large Ibject 
	 - Unstructured data
	 - All file types (images, videos, scripts)
 - Files 
	 - Network file shared in the cloud 
 - Disks
	 - Virtual hard drives for VMs
 - Queues
	 - Asynchronous messageing between apps and services 
 - Tables (..kind of)
	 - NoSQL database storage 
	 - Gradually transitioning to Cosmos DB


## Database and Analytics 
Database - structured data 
Multiple **managed** database services (PaaS)
- Azure SQL, Cosmos DB, PostgreSQL

SQL and NoSQL
Fullty managed 
Single region vs multiple regions 
Open source vs proprietary

## App Service and Serverless Computing