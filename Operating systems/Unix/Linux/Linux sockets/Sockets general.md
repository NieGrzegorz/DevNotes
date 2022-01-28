# Linux sockets 

## What is a socket 
A way to speak to other programs using standard Unix file descriptors

## Types of Internet sockets 
Raw sockets 
- Stream Sockters (SOCK_STREAM)
- Datagram Sockets (SOCK_DGRAM)

### Datagram sockets 
Datagram sockets are sometimes called "connectionless sockets". Datagram sockets use UDP (User Datagram Protocol). They are called connectionless because you don't have to maintain an open connection. Usage: tftp, dhcpcd, multiplayer games, streaming audio, video conferencing. 

To make udp reliable, some protocols require to ACK message to be send with confirmation. If confirmation is not received, the packet is resent. 

There are also unreliable applications (games, audio/video streaming) and dropped packets are ignored or somehow compensated.

Why to use? "Speed and speed"

### Stream sockets 
Stream sockets are reliable two-way connected communication streams. They are error-free. Stream sockets are used in telnet, http. Stream sockets use TCP (Transmission Control Protocol). 

## References 