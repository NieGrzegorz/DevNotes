
## High availability
Ability to maintain continuous performance despite temporary load fluctuations or failures in services, hardware or data centers.

In azure it is based on **redundancy** on every level: 
- Power systems are redundant, power battery backups
- Cooling - different cooling solutions
- Networking - redundant networking HW or ISPs 
- Etc.

Data center - single center with servers 
Availability zone - group of one or more **data centers**
Region encompasses multiple **availability zones** 


## Fault tolerance 
Systems ability to continue operating properly when one or more of its components fails. 

Proactive approaches: 
- Regularly back up data/apps/resources
- Deploy to multiple availability zones or regions 
- Load balance across multiple availability zones or regions 
- Monitor health of data/apps/resources 

Reactive approaches: 
- Restore data/apps/resources to different availability zones or regions 
- Deploy to  different availability zones or regions 

## Disaster Recovery
System's ability to back up and restore data/apps/resources when needed 

We can use Azure to restore: 
- On-premises to on-premises 
- On-premises to Azure 
- Other clout to Azure 
- Azure to Azure


## Scalability and Elasticity 
### Scalability 
Ability to increase the instance count or size of existing resources 

Scaling out (horyzontalne)
- Increase instance count of existing resources 
- Non-disruptive 

Scaling up (Wertykalne)
- Increase instance size of existing resources 
- Disruptive


### Elasticity 
The ability to increase or decrease the instance count or size of existing resources based on fluctuations in traffic or load or in resource workload

- Ability to scale in both directions (in + out up + down)
- Can be manual or automatic 
- Based on changes in load or workload 
- Pay only for what you use 

## Business agility
An organization' ability to rapidly adapt to market and environmental changes in productive and cost-effective ways and take advantage of available resources to meet customer demands. 

- Focus on time to value 
	- Get new products to market as soon as possible 
	- Shorter feedback cycles 
	- Faster return of investment
- Innovation
	- Always look for better way of doing things using newer and better technologies 
- Low latency 
	- The sooner a decision can be acted upon, the sooner the business knows whether the decision was right and what else needs to be done
- Economic effectiveness 
	- Cost effective processes and use of resources
- Rapid adaptation 
	- Continually monitoring and adapting to changing market conditions 
- Flexibility 
	- Move quickly to take advantage of new opportunities