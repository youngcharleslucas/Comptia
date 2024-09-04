
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

