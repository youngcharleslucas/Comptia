# Network Plus Objectives (N10-009) 

## 1.0 Networking Concepts  

### 1.1 Explain Concepts related to the Open System Interconnection (OSI) reference Model  

#### Layer 1 - Physical

#### Layer 2 - Data 

#### Layer 3 - Network  

#### Layer 4 - Session 

#### Layer 5 - Session  

#### Layer 6 - Presentation  

#### Layer 7 - Application  


### 1.2 Compare and contrast networing applicances, applications, and functions  

#### Physical and virtual appliances  

- Router  

- Switch  

- Firewall  

- Intrusion detection system (IDS)

- Intrusion prevention system (IPS)  

- Load balancer  

- Proxy  

- Network-Attached Storage (NAS)  

- Storage area network (SAN)  

- Wireless  

	- Access Point (AP)  
	
	- Controller  
	
#### Applications  

- Content Delivery Network (CDN)  

#### Functions  

- Virtual Private Network (VPN)  

- Quality of Service (QoS)  

- Time to Live (TTL)  


### 1.3 Summarize cloud concepts and connectivity options  

- Network Functions Virtualization (NFV)  

- Virtual Private Cloud (VPC)  

- Network Security Groups  

- Network Security Lists  

- Cloud gateways  

	- Internet gateway  
	
	- Network Address Translation (NAT) gateway  
	
- Cloud Connectivity Options  

	- VPN  
	
	- Direct Connect  
	
- Deployment models  

	- Public 
	
	- Private  
	
	- Hybrid  
	
- Service Models  

	- Software as a Service (SaaS)  
	
	- Infrastructure as a Service (IaaS)  
	
	- Platform as a Service (PaaS)  
	
- Scalability 

- Elasticity  

- Multitenancy  


### 1.4 Explain common networking ports, protocols, services, and traffic types  

| Protocols 						| Ports  	| 
| :---								| :---:		|  
| File Transfer Protocol (FTP) 		| 20/21		|  
| Secure File Transfer (SFTP)		| 22		|  
| Secure Shell (SSH)				| 22		|  
| Telnet 							| 23		|
| Simple Mail Transfer Protocol (SMTP) | 25		|
| Domain Name System (DNS) 			| 53		|
| Dynamic Host Configuration Protocol (DHCP)  | 67/68  |
| Trivial File Transfer Protocol (TFTP) |  69   |
| Hypertext Transfer Protocol (HTTP)  | 80		|
| Network Time Protocol (NTP) 		|	123		|
| Simple Network Management Protocol (SNMP)  | 161/162  |
| Lightweight Directory Access Protocol (LDAP) | 389  |
| Hypertext Transfer Protocol Secure (HTTPS) | 443 |
| Server Message Block (SMB) 		| 445 		|
| Syslog 							| 514		|
| Simple Mail Transfer Protocol Secure (SMTPS) | 587 |
| Lightweight Directory Access Protocol over SSL (LDAPS) | 636 |  
| Structured Query Language (SQL) Server | 1433	|  
| Remote Desktop Protocol (RDP) 	| 3389		|  
| Session Initial Protocol (SIP) 	| 5060/5061 |  

- Internet Protocol(IP) types  

	- Internet Control Message Protocol (ICMP)  
	
	- Transmission Control Protocol (TCP)  
	
	- User Datagram Protocol (UDP)  
	
	- Generic Routing Encapsulation (GRE)  
	
	- Internet Protocol Security (IPSec)  
	
		- Authentication Header (AH)  
		
		- Encapsulation Security Payload (ESP)  
		
		- Internet Key Exchange (IKE)  
		
	- Traffic types  
	
		- Unicast  
		
		- Multicast  
		
		- Anycast  
		
		- Broadcast  
		
### 1.5 Compare and contrast transmission media and transceivers  

- Wireless  

	- 802.11 standards  
	
	- Cellular  
	
	- Satellite  
	
- Wired  

	- 802.3 standards  
	
	- Single-mode vs. multi-mode  
	
	- Direct attach copper (DAC) copper  
	
		- Twinaxial cable  

	- Coaxial cable  
	
	- Plenum vs. non-plenum cable  
	
- Transceivers  

	- Protocol  
	
	- Ethernet  
	
	- Fibre Channel (FC)  
	
- Connector Types  

	- Subscriber connector (SC)  
	
	- Local connector (LC)  
	
	- Straight tips (ST)  
	
	- Multi-fiber push on (MPO)  
	
	- Registered jack (RJ)11  
	
	- RJ45  
	
	- F-Type  
	
### 1.6 Compare and contrast network topologies, architectures, and types  

- Mesh  

- Hybrid  

- Star/hub and spoke  

- Spline and leaf  

- Point to point  

- Three-tier hierarchical model  

	- Core  
	
	- Distribution  
	
	- Access 
	
- Collapsed core  

- Traffic flows  

	- North-south  
	
	- East-west  
	
### 1.7 Given a scenario, use appropriate IPv4 network addressing  

- Public vs. Private  

	- Automatic Private IP Addressing (APIPA) 
	
	- RFC1918  
	
	- Loopback/localhost  
	
- Subnetting  

	- Variable Length Subnet Mask (VLSM)  
	
	- Classless Inter-domain Routing (CIDR)  
	
- IPv4 address classes  

	- Class A  
	
	- Class B 
	
	- Class C  
	
	- Class D  
	
	- Class E  
	
### 1.8 Summarize evolving use cases for modern network environments  

- Software-defined netwrok (SDN) and Software-defined wide area (SD-WAN)  

	- Application aware  
	
	- Zero-touch provisioning  
	
	- Transport agnostic  
	
	- Central policy management  
	
- Virtual Extensible Local Area Network (VXLAN)  

	- Data center interconnect (DCI)  
	
	- Central policy management  
	
- Zero trust architecture (ZTA)  

	- Policy-based authentication  
	
	- Authorization  
	
	- Least privilage access  
	
- Secure Access Secure Edge (SASE)/Security Service Ede (SSE)  

- Infrastructure as code (IaC)  

	- Automation  
	
		- Playbooks/templates/reusable tasks
		
		- Configuration drift/compliance  
		
		- Upgrades  
		
		- Dynamic inventories  
		
	- Source Control  
	
		- Version Control  
		
		- Central Repository  
		
		- Conflict identification  
		
		- Branching  
		
- IPv6 addressing  

	- Mitigating address exhaustion  
	
	- Compatibility requirements  
	
		- Tunneling  
		
		- Dual stacks  
		
		- NAT64  
		
## 2.0 Network Implementation  

### 2.1 Explain characteristics of routing technologies  

- Static routing  

- Dynamic routing  

	- Border Gateway Protocol (BGP)  
	
	- Enhanced Interior Gateway Routing Protocol (EIGRP)  
	
	- Open Shortest Path First (OSPF)  
	
- Route Selection  

	- Administrative distance  
	
	- Prefix length  
	
	- Metric  
	
- Address Translation  

	- NAT  
	
	- Port address translation (PAT)  
	
- First Hop Redundancy Protocol (FHRP)  

- Virtual IP (VIP)  

- Subinterfaces  

### 2.2 

