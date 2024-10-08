
# Open Systems Interconnection (OSI) overview  

**P**lease **D**o **N**ot **T**hrow **S**ausage **P**izza **A**way

| Layer 			|	Attributes				|
| :---				| :---						|
| L7 - Application 	| APIs						|
| L6 - Presentation | Data Conversion			|
| L5 - Session		| Session tracking/naming	| 
| L4 - Transport	| Segmentation/reassembly	|
| L3 - Network		| Router, IP addressing, packets |
| L2 - Data Link	| NIC, Switch, MAC addressing, frames, LLC (Logical Link Control) and MAC (Media Access Control)  |
| L1 - Physical		| Cables, hubs				|  

- A frame encapsulates a packet, packets encapsulate segments

- A general term for encapsulated data in each layer is **protocol data unit** (PDU)  

## Layer 1 - Physical  


## Layer 2 - Data Link

- Anything dealing with the MAC address is part of L2.  

### NIC (Network Interface Card)  

- Mostly part of L2, but is also part of L1 because it is capable of sending 
and receiving physical signals.    

- Contains the Media Access Control (MAC) address. It is burned onto a ROM chip 
on the NIC  

- NIC creates two sublayers inside the L2 Data Link layer: 

	- **Logical Link Control** (LLC): the NIC talks to the operating system, 
	usually through a device driver  
	
	- **Media Access Control** (MAC): creates and addresses the frame.  MAC checks
	the FCS  

### MAC address  

- If is a 48 bit hexadecimal number  

- The first 6 digits are the number assigned to the manufacturer of the NIC.  

- The last 6 digits are the unique serial number to the NIC. This is called 
the **Organizationally Unique Identifier (OUI)**  

- View the physical address, AKA MAC address:

	- Windows `ipconfig /all`  
	
	- Apple ` ifconfig`  
	
	- Linux `ip a`  
	
- MAC-48 is also called EUI-48 by the IEEE, for Extended Unique Identifier  

- **Broadcast address** - `FF-FF-FF-FF-FF-FF` requests the MAC address from all 
devices on the switch.  Happens on L2.  

### Frames  

**Basic elements**:  

| Recipient MAC address | Sender MAC address | Type | Data | FCS | 
| --- | --- | --- | --- | --- |  

- Can also be simplified to **header** (MAC), **payload**, **trailer** (FCS)  

- Ethernet frame types hold at most, 1500 bytes of data  

- Type: indicates what is encapsulated in the frame  

- FCS (frame check sequence): a 4 bytes that indicate are the result of running 
the Data through an equation called **Cyclic redundancy Check (CRC)**. The recipient 
will perform the same equation to verify that all the data is recieved and intact.  

- **Unicast Frame**: does not broadcast, it is a frame that is directed to one 
MAC address  



### Switches

- Filter traffic by MAC address  


## Layer 3 - Network Layer  

- **Logical Addressing**: breaks up networks into subnets, virtually, ignoring 
actual hardware  

- L3 deals with the IP address, not MAC address  

- TCP/IP: protocol suite for logical addressing  

- Contains routers for forwarding data using IP addressing  

- Routers strip off the incoming frame, determines where to send the packet based 
on the IP address, creates a new frame, then sends the packet in the new frame  

### Packets  

- Containers (PDU) for sending data from one network to another, using IP  


## Layer 4 - Transport Layer  

- Segmentation and Reassembly: chops the data into chunks that fit in a packet, 
organize the order of the packets. Reassembly does the opposite.  

- **Segments**: data broken into chunks and given a sequencial number  

- **Datagrams**: data not broken up or given sequencing numbers  

- L4 will re-request packets that were not recieved in good order  

### Connection vs Connectionless protocols  

- UDP (User datagram protocol): connectionless  

- UDP segments in a packet:  

| Source Port | Destination Port | Length | Checksum | Data |  
| --- |  


- TCP (Transmission Control Protocol): connection-oriented  

- TCP segments within a packet:  

| Source Port | Destination Port | Sequence Number | Acknowledgment number | more stuff... | Data |  
| --- | 


## Layer 5 - Session Layer  

- Handles the connection status from one application to another.  

- Check the current status of sessions: 

	- Windows: `netstat -a`  
	
	- Linux: `ss`  
	

## Layer 6 - Presentation Layer  

- Translates data from lower layers to a format that is readable to the 
Applicaiton Layer  

## Layer 7 - Application Layer  

The Operating System provides API for communication with programs, so that 
programmers can make their applications network aware  

## Other  

Accessing information on distributed computers, like BitTorrent file sharing 
protocol, is called **peer-to-peer**

# Network Topologies  

- Bus topologies require terminators to prevent signals from reflecting at the ends  

- Star topology: aka hub-and-spoke, is fault tolerant.  

- *Physical Toplology* is how the cables physically look  

- *Logical Topology* (aka signaling topology) is how the signals actually travel  

- Any form of network technology that combines *physical topology* and 
*logical topology* is a **hybrid topology**  

- Mesh topology: mostly seen in wireless connections. In a *partial mesh* some 
computers may have to traverse through other computers to reach their destination.  


# Ethernet Standards  

![alt text](images/ethernet_standards.png "IEEE Ethernet Standards")  

**Baseband**: only a single signal travles over the wires at a time, occupying the
lowest frequency. (Ethernet networks)  

**Broadband**: multiple signals flow over the same wire at the same time, modulating
to higher frequencies.  (Cable television and cable Internet)  

**Half-duplex**: can send and receive data, but not at the same time  

**Full-duplex**: can send and receive data at the same time. Does not increase 
network speed, but does increase network bandwidth  

**Media Converter**: connect any type of Ethernet cableing together  

**Transceiver/optic**: the connecting module linking the cable to the switch  

**Gigabit interface converter (GBIC)**: modular port for gigabit ethernet  

**Small form-factor pluggable (SFP)**: hot-swappable replacement to GBIC. Take up 
less space.  

![alt text](images/sfp.png)  

**Wave division multiplexing (WDM)**: differentiate the different wave signals on 
a single fiber, creating a *single strand fiber transmission*  

**Single Strand Fiber Transmission**:  

**Bidirectional(BiDi) transceivers**: have only a single optical port designed 
inside to send on one wavelength (like 1310nm) and receive on a different 
wavelength (like 1550nm)  


**Synchronous Optical Network(SONET)**: standardized protocol that transfer 
multiple digital bit streams synchronously over optical fiber using lasers or 
highly coherent light from light-emitting diodes (LEDs). At low transmission 
rates data can also be transferred via an electrical interface.  

**Multisource agreement (MSA)**: agreements amoung multiple manufacturers to make 
interoperable devices and standards    



- All modern NICs are multispeed and auto-sensing  

**Ethernet Connectors**  

![alt text](images/early_ethernet_connections.png)  


### 100BASE-T  

- 100 Mbps  

- **Signal Type**: Baseband  

- **Distance**: 100 m

- **Node Limit**: 1024  

- **Topology**: Star-bus topology; physical star, logical bus  

- **Cable Type** Cat 5 or better UTP or STP cabling with RJ-45/8P8C connectors  

### 100BASE-FX  

- Fiber based networks improve on UTP cabling for three reasons:  

	1) UTP has a limit of 100m  
	
	2) UTP lacks electrical shielding  
	
	3) UTP is easy to tap, not good for high security  
	
- **Speed**: 100Mbps  

- **Signal**: Baseband  

- **Distance**: 2000m, or 2km  

- **Node Limit**: No more than 1024 nodes per hub/switch  

- **Topology**: Star-bus topology: physical star, logical bus  

- **Cable Type**: Multimode fiber-optic cabling (generally OM1) with ST or SC connectors  


### 100BASE-SX  

- Fiber on OM1 or OM2 at 850nm. 

- Used ST, SC, LC connectors  

- LED short distance.  

- Not common anymore  

### Gigabit Ethernet/ 1000BASE-T  

- 1000BASE-T uses four-pair UTP or STP to achieve gigabit performance  

- Max length 100m  

- RJ-45 connector  

- Cat 5e  or 6 UTP  

### 1000BASE-SX  

- multimode fiber-optic  

- max length 220-500m  

- 850-nm wavelength and LED 

- LC connectors  

### 1000BASE-LX  

- long-distance single-mode (5km to 70km)  

- 1300-nm wavelength

## Small Form Factor Fiber Connectors  

- Reasons SFF connectors were created:  
	
	1) ST connectors were relatively large, and required twisting, which is not 
	ideal for fiber cables  
	
	2) SC connectors snap in and out, which was good, but they were still too large  
	
- Mechanical Transfer Register Jack (MT-RJ) was the first created  

![alt text](images/mt_rj.png "MT-RJ Connector")  

- Local connector (LC) was created next  



**Fiber connection contact types**:  

![alt text](images/connection_contact_points.png)  

- Flat  

- Physical contact (PC)  

- Ultra-physical contact (UPC)  

- Angled physical contact (APC)  

	- 8 degree angle  
	
### Fiber based 10 GbE  

- Typical transceiver in 10GbE is **Enhanced Small Form-Factor pluggable (SFP+)**  

- R for LAN-based signal  

- W for SONET/WAN-based signaling  

| Standard | Fiber Type | Wavelength | Physical Layer Signaling | Maximum Signal Length |  
| :--- | 
| 10BASE-SR | Multimode | 850nm | LAN | 33-400 m |
| 10BASE-SW | Multimode | 850nm | SONET/WAN | 33-400 m |

- OM1 is 33m range, OM4 is 400m range  

**Long wavelength**  

| Standard | Fiber Type | Wavelength | Physical Layer Signaling | Maximum Signal Length |  
| :--- | 
| 10BASE-LR | Single-mode | 1310nm | LAN | 10 km |
| 10BASE-LW | Single-mode | 1310nm | SONET/WAN | 10 km |  

**Extra Long Wavelength**  

| Standard | Fiber Type | Wavelength | Physical Layer Signaling | Maximum Signal Length |  
| :--- | 
| 10BASE-ER | Single-mode | 1550nm | LAN | 40 km |
| 10BASE-EW | Single-mode | 1550nm | SONET/WAN | 40 km |   

**Copper-Based 10GbE**  

- Cat 6, 55m Max

- Cat 6a, 100m max  

### Fiber Transceivers  

- BiDi advantages over single strand fiber transmission:  

	- Cost less, only need half the cabling  
	
	- use existing fiber runs to rapidly double the capacity of a network

### Backbones

- Multispeed Ethernet networks work best for giving users the fastest network 
response  

- High-speed switches maintain the backbone of the network.  No computers, other
than possibly servers, attach directly to this backbone.

- Requires switches with dedicated high-speed ports  

![alt text](images/backbone.png)


### 40GbE and 100GbE

- 40GbE BiDI tranceivers use **quad small form-factor pluggable (QSFP)** optics  

- 40GbE runs on OM3 or better multimode fiber, uses laser light, uses four channel 
connectors.  

- 40GbE running on Cat 8 UTP max range of 30m, called 40BASE-T  

- 100GbE employ MMF and SMP with various connectors.  

- 100GbE uses a QSFP28 connector that has four channels of 25 Gb each. Also 
called QSFP100 or 100G QSFP  


# Intalling a physical Network  

**Structured Cabling**: set of standards and proprietary systems  

- In the US, these are mostly defined by the **Telecommunications Industry Association**  
(TIA) standards  

- *Building Industry Consulting Service International (BICSI* provides a series 
of widely recognized certifications and training  

- Components of structured cabling: 

	1) Telecommunications Room or Intermediate Distribution Frame (IDF)  
	
	2) Horizontal cabling or runs  
	
	3) Work area(s)  
	
- Horizontal cable is Cat 5e or better UTP for copper 1000BASE-T.  Fiber-based 
1000BASE-SX use multimode fiber-optic cable. Network installations today favor Cat 6    

**Solid Core UTP**: better conductor, but is stiff and will break if  handled too 
often  

**Stranded Core UTP**: not as good of a conductor, but will stand up to substantial 
handling  

- Horizontal cabling should always be solid core  

- All UTP cables are 4-pair UTP now  

- Equpment racks are 19" wide, and measured in *units* (U). Each U is 1.75". A 
rack that is 42U has a height of 42 units  

**two-post rack**: smaller equipment rack  

**four-post rack**: larger equipment rack  

**server rail**: allows you to pull out the server for maintenance, like replace 
dead drives  

**power distribution unit (PDU)**: used in larger racks for cetralized power 
management. Better PDUs enable remote connectivity and management for power 
monitoring.  

- **locking racks** and **locking cabinets** are terms for chassis and doors on 
racks with locking mechanisms  

### Patch Panels and Cables  

**Patch panels**: box with a row of femal ports in the front and permanent connections 
in the back to which you connect horizontal cables (solid core).  

- Most common type of patch panels are 110 block. Older patch panels were 66 block 
for telephone installation  

- All patch panels have a space in front for labels. A standard for labeling 
patches is *ANSI/TIA-606-C*  

- Buy Cat 6 patch panels. They handle 250-MHz. Buying a cheaper patch panel for 
a lower Cat rating will eliminate any gains made by installing Cat 6 runs. Cat 6 
panels also offer lower crosstalk and network interference  

- **Patch Cables**: are straight-through UTP cables that connect the patch ports 
to the switch. These are stranded core. The is also used to connect the PC to the 
wall outlet.    

- Some prefer to buy premade patch cables instead of making them so that they 
have more options for color schemes  

**Patch bay**: dedicated block with Audio/Visual connections rather than twisted 
pair and fiber network connections  

- TIA/EIA 568 specification allows only UTP cable lengths of 90 meters, this is 
to account for patch cables used to connect PCs to the wall with patch cables. 
This is not to exceed the Cat 6 length limit of 100m  

- Most telephone installation will use 25-pair UTP cables running to a 66 block 
to a telecommunications room on each floor  

### Demarc  

**Demarc (demarcation point)**: physical location of the connection and marks the 
dividing line of responsibility. Located in the **service-related entry point**.  

**Network Interface Unit (NIC)**: in private homes, the device supplied by the 
ISP that serves as the demarc  

**Smartjack**: sets up remote loopback enabling internet suppliers to diagnose 
faults in the system   

**Customer-Premises equipment (CPE)**: The device that networks connect to after 
the demarc for building distribution  

**Demarc Extension**: cabling running from the NIU to whatever CPE is used 
by the customer. This connects to a powerful switch, which connects to the  main patch 
panel (vertiacal cross-connect)  

**Vertical Cross-connect**: Main patch panel that connects to all other patch panels  

**Fiber distribution panel**: Fiber patch panel   

**Main Distribution Frame (MDF)**: room where the demarc, LAN cross-connects exist  

### Pulling cable  

- Local codes, TIA, and the National Electrical Code (NEC) have rules about how 
you pull cabling  

- **Low-voltage mounting bracket**: installed on the opening on the wall created 
in the sheetrock for a patch  

- 110-punchdowns connections are used on the back of the wall jack  

### Rolling your own patch cable  

1) Cut the cable square using RJ-45 crimpers or scissors  

2) Strip at least 1/2 inch of plastic jacket from the end of the cable with a 
dedicated cable stripper or the one built into the crimper tool  

3) Insert each individual wire into the correct location according 
to either T568A or T568B, unravel as little as possible  

4) Insert the crimp into the cripmer and press. The crimper has a stop 
to prevent you from using too much pressure  

### Connecting to the patch panel  

- **Plastic D-rings** guide the patch cables neatly along the sides and front of the 
patch panel  

- **Finger Boxes**: rectangular slots in the front; the patch cables run into the open 
ends of the bock, and individual cables are thread through the fingers on their 
way to the patch panel 

### Testing Cable Runs  

- Verify that the cable can handle the speed of your network  

- Three basic issues with Layer 1:  

	- Signal degredation  
	
	- Lack of connection  
	
	- Interference  
	
- Open or short of a cable both cause no connectivity  

- **Split pair**: the signal from any of the pairs in the same cable interfer 
with another pair.  

- **Cable tester**: verify that both ends are terminated correctly  

	- **Continuity Tester**  
	
	- **Wire Map**: tests all the wires on both ends of the cable connect to the 
	right spot. Can find shorts and crossed wires.  
	
	- **Multimeter**: Test AC and DC voltage, current, continuity, and resistance  
	
		- Zero Ohms indicate continuity, infinite Ohms mean no connection  
		
	- **Time-domain reflectometer (TDR)**: can tell you where a break is located  
	
- **Crosstalk**: Signal sent down one pair is picked up by neighboring pairs  

	- Poor crimp can cause increased crosstalk  
	
	- **Near-end Crosstalk (NEXT)**: crosstalk occuring on the signalling end  
	
	- **Far-end Crosstalk (FEXT)**: crosstalk occuring on the opposite end of signal  
	
	- FEXT and NEXT are measured in decibels. You want lower decible. **Decibel**
	**loss** is a way to measure signal loss.  
	
- **Attenuation**: the signal growing gradually weaker as it traverses the cable  

- **Latency**: delay of Ethernet frames traversing the cable from sender to receiver  

- **Jitter**: delay in completing a transmission of all the frames in a message. 
This can be due to a large amount of machines on the network. Video chats will 
appear jittery  

- **Cable Certifiers**: High end testing device that can generate reports and 
certificates for the performance of installed cables   

- **Coupler**: small device with two female ports that enable you to connect two 
pieces of cable together to overcome distance limitations  

- **Toner**: used to trace cables, a tool that is composed of two devices. 
The **tone generator** connects to the cable with alligator clips or a network 
jack, then sends electrical signal down the wire. The **Tone Probe** will make 
a noise when it is placed near the wire with the signal  

### Causes of poor Fiber Signal    

- Damaged Cables or open connections  

- Dirty connectors  

- Connector mismatch 

- Attenuation   

- **Dispersion**: signal spreads out over long distance. Also called **modal**
**dispersion**, where dispersion or attenuation is caused by signals traveling 
too far without help  

- Exceeding the **bend radius limitation**.  Too much bend, and the light will 
escape through the bend, called **light leak**.  

- Incorrect transceiver/ tranceiver mismatch: different manufacturers may be 
incompatible  

- Cable mismatch, fiber mismatch, incorrect cable type  

- Wavelength mismatch: the switch may expect 1310nm, but the signal sent is 
1530nm  

- **Optical Time-domain Reflectometer (OTDR)**: finds the location of a break in 
a fiber cable  

- **fusion splicer**: allows for the connection of two fiber-optic cables without
losing quality  


### NICs  

- all Ethernet NICs us RJ-45

- The Expansion slot used on PCs to install a NIC is the PCIe  slot, either one 
or two lanes  

- **Port Aggregation, Link Aggregation, Bonding**: putting multiple NICs in one 
switch to increase the bandwidth  

- **Link Aggregation Control PRotocol (LACP)**: controls how multiple network 
devices send a receive data as a single connection  


### Problems in the IDF  

- UPS have two types, online (which is continuously supplying power to the machine) 
and standby (senses when AC power is lost, then will switch to suppling power from 
the battery)  

- ** Voltage Event Recorder**: plugs into the power outlet and tracks the voltage 
over time.  


# TCP/IP Basics  

**Internet Protocol (IP)**: works on the Network Layer  

**Internet Control Message Protocol (ICMP)**: is a TCP/IP, plays a role in error 
reporting and diagnostics. Used by the `ping` utility.  

**Simple IP header**:  

| Ver | IHL | DSCP | ECN | Total Length | TTL | Protocol | ... |  
| :---: |

- Version: IPv4 or IPv6  

- Total Length: Total size of the IP packet in octets, including the IP header and 
payload. This field is 16 bits. Limits the packet size to 65 KB.  

- Time to Live (TTL): Prevents the packet for endlessly spinning through the 
internet. Has a counter that decrements everytime the packet goes through a 
router. Cannot start higher than 255, most start at 128.  

- Protocol: either TCP or UDP  

### Transport Layer Protocols  

**Transmission Control Protocol (TCP)**: connection-oriented  

- TCP three-way handshake: SYN, SYN-ACK, ACK  

- TCP chops data into segments, segments get a sequence number. The receiving system 
will request a segment if it was missing.  

- TCP Header:  

| Souce port | Destination port | Sequence Number | Acknowledgement number |  
| :---: |

- **Sequence number and Acknowledgement Number**: enable the sending and receiving 
computers to keep track of the various pieces of data flowing back and forth.  

- **Flags**: The individual bits give both sides detailed information about the 
*state of the connection*  

- **Checksum**: check the TCP header for errors

**User Datagram Protocol (UDP)**: connectionless  

- Used by *Domain Name System (DNS)* and *Dynamic Host Configuration Protocol (DHCP)*  

- UPD Header:  

| Source Port | Destination Port | Length | Checksum |  
| :---: |  

- UDP does not chop up data, but sends it as a *datagram* (Not a segment like TCP)  

At the LAN level, every host runs TCP/IP software over Ethernet hardware  

To get other computer's mac address, a broadcast is sent out by the requesting 
client. It is called **ARP request or Address Resolution Protocol** to MAC 
address FF-FF-FF-FF-FF-FF. The switch will broadcast this to every connected node.  

- In Windows, the ARP cache can be seen with the command `arp -a`  

IPv4 are 32 bit values.  Normally written in **dotted decimal notation**  

A WAN is nothing more than two or more connected LANs.  For a WAN to work, each LAN  
needs some form of unique identifier called a **network ID**. It will usually 
have a host ID of all 0s.

Every TCP/IP LAN that wants to connect to another TCP/IP LAN must have a router.  

**Default Gateway**: a term for both the router itself and the router's interface 
on the LAN.  

- To connect the network beyond the router, you use the IP address of the 
default gateway.

- The default gateway is usually configured to be the lowest or highest host address.
So for a network ID of 22.33.4.x, the default gateway could be 22.33.4.1 or 
22.33.4.254.

Two NIC router, common in many homes. One NIC connects to the LAN, the other 
connects to the Internet Service Provider's network. Built into this router is 
a routing table.  

- **Routing Table**: instructions that tell the router what to do with incoming
packets and where to send them.  

- No two LANs can share the same network id 

- The highest host id (all 255) is used as a **boradcast address**, that will 
talk to every computer on the LAN  

**Subnet Mask**: tells the sending computer if the IP address is local or long 
distance.  The subnet mask represents the ones as the network id and the 
**host ID** are the 0s.  

`11111111111111111111111100000000`  

is the binary representation of dotted decimal `255.255.255.0` subnet mask.  

- If a sending computer knows that the recipient is local, because they share 
the same network id from the known subnet mask, then the sending computer can 
broadcast for a MAC address with ARP, Address Resolution Protocol.  

- Whenever a computer wnts to send to an IP address on another LAN, it knows 
to send the packet to the default gateway. It still sends out an ARP broadcast,
but this time it's to learn the MAC address for the default gateway.  

Most representations of subnet masks are done with CIDR notation:  
```
11111111111111111111111100000000 = /24  
11111111000000000000000000000000 = /8  
```  

This shows the IP address and the subnet mask in one address  

### Class IDs

**Internet Assigned Numbers Authority (IANA)**: tracks and disperses IP addresses  

- IANA oversees 5 **Regional Internet Registries (RIR)** that parcel out IP 
addresses to ISPs and corporations.  

- The RIR for North America is **American Registry for Internet Numbers (ARIN)**  

|     		| First Decimal	| Addresses 				| Hosts per Network ID	|  
| :---		|  
| Class A	| 1-26			| 1.0.0.0-126.255.255.255	| 16,777,216			|  
| Class B	| 128-191		| 128.0.0.0-191.255.255.255	| 65,534				|  
| Class C 	| 192-223		| 192.0.0.0-233.255.255.255	| 254					|  
| Class D 	| 224-239		| 224.0.0.0-239.255.255.255 | Multicast				|  
| Class E 	| 240-255		| 240.0.0.0-255.255.255.255	| Experimental			|  

Remember to subract 2 from the IP block for the network id and broadcast address.  

There are 4 ways to send a packet:  

- *Broadcast*: which is where every computer on the LAN hears the message  

- *Unicast*: where one computer sends a message directly to another  

- *Anycast*: where multiple computers share a single address and routers direct 
the messages tot he closest computer.  

- *Multicast*: where a single computer sends a message to a group of interested 
computers.  

Routers *Multicast* to talk to eachother.  

Class IDs did not scale well, so CIDR was created  

### CIDR and Subnetting  









	
	



