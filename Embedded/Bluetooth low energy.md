# Bluetooth low energy (BLE)

Version 4.2 of the Bluetooth specification describes two systems of wireless technology
- Basic Rate (BR: BR/EDR for Basic Rate/Enhanced Data Rate)
- Bluetooth low energy (BLE) 

## BLE vs classic Bluetooth (BR/EDR)
- BLE focuses on low power consumption
- ISM BAND 2.4 GHZ - like wifi or classic bluetooth
- Radio spectrum split into 40 channels - 3 primary advertising channgels 
- BLE is incompatible with BR/EDR
- BLE for data transfer which is bursty and has lower bandwidth
- Most new features and updates in bluetooth specification are targeted at BLE 

## Properties of BLE 
- Range - varies on configurations - few meters to over 1 km (with Forward errror corection)
- As low power consumption as possible achieved by turning of radio communication as often as possible. Turning on to send or receive data and then to Sleep asap. 
- Data throughput - 2Mbit is max for radio, BLE can achuieve up to 1.4 Mb
- Adaprivae Frequency Hopping - allows to dynamicly avoid colision and interference with other devices and signals in 2.4 GHZ 

#### Advantages :
- Open spec 
- Support of smartphones and others 

### Most important concepts in BLE
#### Peripherals and Centrals
Peripheral is a device which sends advertisment data for other devices to discover it (to connct to it or just to read its advertised data ). 

Cenral is a device which discovers thes advertisments packets it could connect to device if advertisments data allows. Bluetooth beacon is a device which advertises data and does not allow to connect to it (used in retail marketing, indoor navigation). 

Central takes heavy lifting, consumes more power, central can have connection to multiple peripherals and peripherals can be connected to different centrals. Some devices can act  as centrals and peripherals. 

#### Advertising and scanning 
Advertising mode is when a peripheral sends data called **advertisment packets** for other devices to discover it. It could lead to a connection or just simply for discovery and reading. It does that by sending advertisment packets to 3 primary advrtisment channels. The central will be continously scanning the 3 primary advertisment channels looking for advertising packets from other devices. There are different types of advertisment packets used - some of them allow connections other does not allow connections and some allow for discovery and connections. Kind of data sent in advertisment packets: 
- Device name 
- TX power level 
- Services supported by device 
- Apperance ID - identifies type of device 

Key parameter of peripheral 
Advertising interval - important 20ms - 10,24sec

Key parameter of centrals 
Scan window: how long to scan for advertising packets
Scan interval:How often to scan for adcertisment packets 
#### Conenctions 
In order to connect: 
- Peripheral has to send an connectible advertisment packet
- Central has to scan for advertisment packet on primary advertisment channels 
- When central sees a connectible advertisment packet it will send out a connection request to ther peripheral 
- Once a peripheral receives a request it will respond with a packet
- When a central receives a packet, a connection is considered to be established 

Three most important parameters related to the connections: 
- Connection interval - how often a peripheral and a central exchange data with each other 
- Peripheral latency ( used to be called slave latency) - allows a peripheral to SKIP several connection intervals without the central dropping the connection 
- Supervision timeout - detect and determine when connection to a peripheral is lost 
#### Services and characteristics 
Called attributes. Define how the BLE device organizes and structes data that it exposes to other devices to discover. 

Sensor readings, sensor data, 

Service - grouping of one or more charecteristics (logical groupins). Related characteristics are often grouped in a service. 

## Texas Instruments BLE stack 

### Features 
- LE Secure connections 
- LE Data Length extension 
- LE Privacy 1.2 
- LE L2CAP Connection-Oriented Cahnnel Support 
- LE Link Layer Topology 
- LE Ping 
- Slave Feature Exchange 
- Connection Parameter Request 

### Basics 
BLE protocol stack consists of the **controller** and the **host**. This separation derives from the implementation of classic Bluetooth BR/EDR devices where two sections are implemented separately. Any profiles and applications sit on top of the [[GAP]] and [[GATT]] layers of the protocol stack. 

#### Generic Access Profile (GAP)
Controls the RF state of the device, with the device in one of five states: 
- Standby 
- Advertising 
- Scanning 
- Initiating 
- Connected 



#### The Application 
- TI RTOS is used 
- In application SYS/BIOS kernel scheduler is started with interrupts enabled. 

#####  Indirect Call Framework (ICall)
Module that provides a mechanism for the application to interface with the Bluetooth low energy protocol stack services as well as certain primitive services provided by TI-RTOS (i.e. thread synchronization). 
- that the ICall module must be initialized by [ICall_init()](https://software-dl.ti.com/lprf/simplelink_cc2640r2_sdk/1.00.00.22/exports/docs/blestack/doxygen/group___i_call.html#ga7ff723a346156b189a6700cb2cc297c8) and the stack task is created via [ICall_createRemoteTasks()](https://software-dl.ti.com/lprf/simplelink_cc2640r2_sdk/1.00.00.22/exports/docs/blestack/doxygen/group___i_call.html#ga9c6d55cb8b177a15796006d20f8634d6).
- ICall allows the application and protocol stack to operate efficiently, communicate, and share resources in a unified TI-RTOS environment.
- the ICall core use case involves messaging between a server entity (that is, the BLE-Stack task) and a client entity (for example, the application task).
- The ICall framework is not the GATT server and client architecture, as defined by the Bluetooth Low Energy protocol. *WAŻNE*

REASONING BEHIND SUCH ARCHITECTURE 
-   To enable independent updating of the application and Bluetooth Low Energy protocol stack
-   To maintain API consistency as software is ported from legacy platforms (that is, OSAL for the CC254x) to TI-RTOS of the CC2640R2F.

