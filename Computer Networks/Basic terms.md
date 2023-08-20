# Basic terms 

# The Internet
[[The Internet]] is a computer network that connects billions of computing devices called [[hosts]] or [[end systems]]. End systems are connected together by a network of [[communication links]] and [[packet switches]]. 

The Internet may be defined also as an infrastructure that provides services to applications. This applications are said to be distributed applications since they involve 


### Packet switch
A packet switch takes a packet arriving on one of its incoming communication links. Most popular packet switches in today's internet are [[routers]] and [[link-layer switches]]. Both types of switches forward packets towards their ultimate destinations. 
[[Communication link]]

Route or path is the sequence of communication links and packet switches traversed by a packed from the sending end system to the reviving end system. 

[[Internet Service Provider]]

### Protocol 
End systems, packet switches and other pieces of the Internet run protocols that control the sending and receiving of information withing the Internet. The most important ones are [[Transmission Control Protocol]] and [[Internet Protocol]].

### Request for comment  (RFC)
The Internet standards are developed by the Internet Engineering Task Force. Their documents are called requests for comments. They define the protocols and other network stuff

"A protocol defines the format and the order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission and/or receipt of a message or other event"

End systems attached to the [[Socket interface]] that specifies how a program running on one of end systems asks the Internet infrastructure to deliver data to a specific destination program running on another end system.


### How homes connect to the Internet? 
Digital subscriber line (DSL) and cable. 
#### DSL
A household usually obtains DSL Internet access from the same lical telephone company (telco) that provudes its wired local phone access. So if DSL is used a customers telco is also its ISP. 

In this case, each DSL modem uses the existing telephone line ti exchange data with a digital subscriber line access multiplexer (DSLAM) located in telco's central office. DSL modem takes digital data and transates it to high-frequency tones for transmission over telephone wires. These are translated back to digital format at the DSLAM. 

"Engineers have expressly designed DSL for short distances between the home and the CO; generally, if the residence is not located within 5 to 10 miles of the CO, the residence must resort to an alternative form of Internet access."

#### Cable Internet access
Uses the same infrastructure from cable television provider. 

Fiber and coaxial cables are used called hybrid fiber coax (HFC)
- Requires special modems called cable modems 

#### FTTH (Fiber to the home)
Optical fiber path from the CO directly to the home. 


### Physical media 
- HFC - combination of fiber calbe and coaxial cable 
- DSL and Ethernet - copper wire
- Mobile - radio spectrum 

How a bit is transfered between end systems? 
For each transmitter-receiver pair, the bit is sent by propagating electromagnetic waves or optical pulses across a physical medium

types of physical media: twisted-pair copper wire, coaxial cable, multimode fiber-optic cable, terrestual radio spectrum, satelite radio spectrum. 

There are 2 groups of physical media: guided and unguided 

Essentials: 
Packet switching 
Circuit switching 
Bandwidth

"+ With FDM, each circuit continuously gets a fraction of the bandwidth. With TDM, each circuit gets all of the bandwidth periodically during brief intervals of time (that is, during slots)"


### Types of delay in packed switched networks
- Processing delay - The time required to examine the packet's header and determine where to direct thte packer. In high-speed routers are on the order of microseconds or less. After processing packet does to queue. 
- Queuing delay - time when packet waits in queue ti be transmited onto the link. Depends on number of packet waiting. Order of microseconds to miliseconds in practice. 
- Transmission delay - L bits, R is rate (bits/second). Transmission delay is L/R. It is the amount of time needed to transmit all of the packet bits into the link. Microseconds to miliseconds. 
- Propagation delay - Time required to propagate from the beginning of the link to the next router. The bit propagates at the propagation speed of the link. Depends on the physical medium (fiber optics, copper wire). Propagation delay is the distance between 2 routers divided by the propagation speed. 

#### Transmission delay vs Propagation delay
Transmission delay - time required by the router to push packets into the link, it has nothing to do with a distance between routers 
Propagation delay - time required to transmit over the medium to the next router. 
