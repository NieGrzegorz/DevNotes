
Cloud computing - on demand availability of computer system resources split into 3 main categories 
- Computing 
- Networking 
- Storage 

It involves data centers located around the world. 

## The language of cloud computing 
- High availability 
	- Core to the cloud 
	- If server fails it is replaced instantly 
	- Use clusters to ensure high availability 
- Reliability - Fault tolerance, disaster recovery
	- Resilience 
	- System can recover from failures and continue to functions 
	- Strategies: 
		- Deploy in Multiple Locations - protects against regional failures 
		- No single point of failure - if one computers goes down it is replaced 
- Scalability - scaling up or down on demand 
	- Increase number of VMs to handle peak traffic
	- Automatically reduce resources on demand 
	- Scaling - Horizontal is the most popular: 
		- Horizontal - Adding more VMs/containers (Scaling out) 
		- Vertical - Increasing power (e.g. CPU/RAM) of existing VMs (Scaling up)
		
- Security - full control for security of environment. Patches, maintenence, network control
- Predictability - predictable performance and costs 
	- Performance - consistent experience for customers regardless of traffic
	- Autoscaling, load balancing, and high availability provide a consistent experience 
	- Costs - no unexpected costs 
		- Tracks and forecasts costs 
- Governance - standardized environments, regulatory requirements, audit for compliance
- Manageability 
	- Management of the cloud - autoscaling, monitoring, template based deployments 
	- Management in the cloud - CLI, Portal, APIs

## The economy of cloud computing 
- Capital expenditure (CapEx)- Money spent by a business or organization on acquiring or maintaining fixed assets such as land, buildings and equipment. 
	- Large upfront investments 
- Operational expenditure (OpEx) - An ongoing cost for running a product, business, or a system on a day-to-day basis, including annual costs. 
	- Pay as you go
		- Per execution, per second or combination of these (consumption-based pricing)
## Cloud service models 

IaaS 
Infrastructure = actual servers 
Scaling is fast
No ownership of hardware 

PaaS - superset of IaaS 
PaaS supports web application life cycle 
Avoids software license hell 

SaaS 
Providing a managed service 
Pay an access fee to use software 
No maintenance and latest features 

Serverless - you dont have to manage the serverless 
Azure functions is the best known serverless service 
Extreme PaaS 

## Azure marketplace 
## Cloud Architect Models 
Public cloud 
- No purchase of hardware 
- Low monthly fees 
- Accessed from anyware 
- No control over features 

Hybrid cloud 
- Avoid disruptions and outages 
- Adhere to regulations, governance 
- Span both public and private cloud 
- Alleviate CapEx investments 
- Complex infrastructure 

Private cloud 
- Full control on your servers 
- A lot of staff required 

