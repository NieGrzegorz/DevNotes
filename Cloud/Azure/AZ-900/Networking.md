

Virtual network (VNet) - Enables vms to securly connect to internet. It is virtual because you dont have access to a hardware. 
- Address space - range of addresses available, every service or resource that is in vnet will get an address from address space in vnet. 
- You can segment vnet to have multiple address spaces and virtual subnets. You can secure subnets. 
- Bnet belongs to a single region 
- Vnet belong to single subscription 
Advantages of vnets: 
- Scaling - add more vnets 

VNet Peering 
- Low latency, high bandwidth 
- Link separate networks 
- data transfer 

Load balancer 
inbound flow - traffic from the internet or local network 
Backend pool - th vm instances receiving traffic 

VPN Gateway - send encrypted thata through secure tunnel


Application Gateway = load balancer + cloud. Based on different parameters than ip address. 
- Http address 
- Data format : 
	- URI 
	- Host header

Contend Delivery Network - keeps copy of app on egde nodes 
Benefits of cdn: 
- Better performance 
- Large scaling 
- Distribution 