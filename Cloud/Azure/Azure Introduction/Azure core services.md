## Virtual Machines 
VMs are part of infrastructure as a service. 

Why to use VMS instead Managed Services? 
- Flexibility 
	- Trade-off - flexibility vs less management 


Availability set - automatic replication of VM over different availability zones 
IF VM goes down, a copied VM can take over 

Scale sets 
- Multiple copies of VMs 
- Goes with load balancer 
- Scaling copies of application 
- Enables scaling and elasticity 

## Networking 
How are VMs and services communicate with outside world 

### Virtual networks 
Virtual Network (VNet) - Fundamental Building Block 
- Provides private and public network communication among Azure resources 
- Uses familiar network concepts in virtual format (subnets, firewalls, routes )
- Virtual format - Software Defined Networking 
- Enables public access or extend private networking to other networks 


## Storage
All purpose storage solution for multiple data storage scenarios 
- Scalable 
- Managed infrastructure 
- Flexible access options 
Types: 
 - Blob
	 - Object storage 
	 - Binary Large Object 
	 - Unstructured data
	 - All file types (images, videos, scripts)
 - Files 
	 - Network file shared in the cloud 
 - Disks
	 - Virtual hard drives for VMs
 - Queues
	 - Asynchronous messaging between apps and services 
 - Tables (..kind of)
	 - NoSQL database storage 
	 - Gradually transitioning to Cosmos DB


## Database and Analytics 
Database - structured data 
Multiple **managed** database services (PaaS)
- Azure SQL, Cosmos DB, PostgreSQL

SQL and NoSQL
Fully managed 
Single region vs multiple regions 
Open source vs proprietary

## App Service and Serverless Computing

## Subscriptions
Subscription covers resources and multiple azure regions and can consist of multiple tenants, resource groups and resources. You can have multiple subscriptions. 

Azure regions are data centers tied to geographical location. 

Tenant == Azure Active Directory


## Active directory
You have set of user credentials and within active directory you have info about users and controls accesses. 

So they moved it to Azure - it helps to link user credentials to access azure 

You use the same credentials for email, azure, dropbox and other services used by business. You can give permissions to users. B2c active directory to house user credentials provided by other social credential providers as google or facebook. 

Developers can offload the task of managing users and the privacy concerns around their data. You can focus on core product development. 

It allows you to have a single source of truth for all of your business applications. 