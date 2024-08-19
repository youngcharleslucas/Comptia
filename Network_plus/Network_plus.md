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

### 2.2 Given a scenario, configure switching technologies and features  

- Virtual Local Area Network (VLAN)  
	
	- VLAN database  
	
	- Switch Virtual Interface (SVI)  
	
- Interface configuration 

	- Native VLAN  
	
	- Voice VLAN  
	
	- 802.1Q tagging  
	
	- Link Aggression  
	
	- Speed  
	
	- Duplex  
	
- Spanning tree  

- Maximum transmission unit (MTU)  

	- Jumbo frames  
	
### 2.3 Given a scenario, select and configure wireless devices and technologies  

- Channels  

	- Channel width  
	
	- Non-overlapping channels  
	
	- Regulatory impacts  
	
		- 802.11h  
		
- Frequency options  

	- 2.4 GHz 
	
	- 5 GHz  
	
	- 6 GHz  
	
	- Band steering  
	
- Service set identifier (SSID)  

	- Basic service set identifier (BSSID)  
	
	- Extended service set identifier (ESSID)  
	
- Network types  

	- Mesh Networks  
	
	- Ad hoc  
	
	- Point to Point  
	
	- Infrastructure  
	
- Encryption  

	- Wi-Fi Protected Access 2 (WPA2)  
	
	- WPA3  
	
- Guest networks  

	- Captive portals  

- Authentication  

	- Pre-shared key (PSK) vs Enterprise  
	
- Antennas  

	- Omnidirectional vs. Directional  
	
- Autonomous vs. lightweight access point  


### 2.4 Explain important factors of physical installations  

- Important installation Implications  

	- Locations  
	
		- Intermediate distribution frame (IDF)  
		
		- Main distribution frame (MDF)  
		
	- Rack size  
	
	- Port-side exhaust/intake  
	
	- Cabling  
	
		- Patch panel  
		
		- Fiber distribution panel  
		
	- Lockable  
	
- Power  

	- Uninterruptible power supply (UPS)  
	
	- Power distribution unit (PDU)  
	
	- Power Load  
	
	- Voltage  
	
- Environment Factors  

	- Humidity  
	
	- Fire suppression  
	
	- Temperature  
	

## 3.0 Network Operations  

### 3.1 Explain the purpose of organizational processes and procedures  

- Documentation  

	- Physical vs. Logical Diagrams  
	
	- Rack diagrams 
	
	- Cable maps and diagrams  
	
	- Network diagrams  
	
		- Layer 1  
		
		- Layer 2  
		
		- Layer 3  
		
	- Asset inventory  
	
		- Hardware  
		
		- Software  
		
		- Licensing  
		
		- Warranty support  
		
	- IP address management (IPAM)  
	
	- Service-level management (SLA)  
	
	- Wireless survey/heat map  
	
- Life-cycle management  
	
	- End-of-life (EOL)  
	
	- End-of-support (EOS)  
	
	- Software management 
	
		- Patches and bug fixes  
		
		- Operating System (OS)  
		
		- Firmware  
		
	- Decommissioning  
	
- Change Management  

	- Request process tracking/service request  
	
- Configuration management  

	- Production configuration  
	
	- Backup configuration  
	
	- Baseline/golden configuration  
	
### 3.2 Given a scenario, use network monitoring technologies  

- Methods  

	- SNMP  
	
		- Traps  
		
		- Management information base (MIB)  
		
		- Versions  
		
			- v2c  
			
			- v3  
			
		- Community strings  
		
		- Authentication  
		
	- Flow data  
	
	- Packet capture  
	
	- Baseline metrics  
	
		- Anomaly alerting/notifications  
		
	- Logan aggregation  
	
		- syslog collector  
		
		- Security information and even management (SIEM)  
		
	- Application programming interface (API) integration  
	
	- Port mirroring  
	
- Solutions  

	- Network discovery  
	
		- Ad hoc  

		- Scheduled  
		
	- Traffic analysis  
	
	- Performance monitoring  
	
	- Availability monitoring  
	
	- Configuration monitoring  
	
### 3.3 Explain disaster recovery (DR) concepts  

- DR metrics  

	- Recovery point object (RPO)  
	
	- Recovery time objective (RTO)  
	
	- Mean time to repair (MTTR)  
	
	- Mean time between failure (MTBF)  
	
- DR sites  

	- Cold site 
	
	- Warm site  
	
	- Hot site  
	
- High-availability approaches  

	- Active-active  
	
	- Active-passive  
	
- Testing  

	- Tabletop exercises  
	
	- Validation tests  
	
### 3.4  Given a scenario, implement IPv4 and IPv6 network services  

- Dynamic addressing  

	- DHCP  
	
		- Reservations  
		
		- Scope  
		
		- Lease time  
		
		- Options  
		
		- Relay/IP helper  
		
		- Exclusions  
		
	- Stateless address autoconfiguration (SLAAC)  
	
- Name resolution  

	- DNS  
	
		- Domain Name Security Extensions (DNSSEC)  
		
		- DNS over HTTPS (DoH) and DNS over TLS (DoT)  
		
		- Record types  
		
			- Address (A)  
			
			- AAAA  
			
			- Canonical name (CNAME)  
			
			- Mail Exchange (MX)  
			
			- Text (TXT)  
			
			- Nameserver (NS)  
			
			- Pointer (PTR)  
			
		- Zone types  
		
			- Forward  
			
			- Reverse  
			
		- Authoritative vs. non-Authoritative  
		
		- Primary vs. Secondary  
		
		- Recursive  
		
	- Hosts Files  
	
- Time protocols  

	- NTP  
	
	- Percision TIme Protocol (PTP)  
	
	- Network Time Security (NTS)  
	

### 3.5 Compare and contrast network access and management methods  

- Site-to-site VPN  

- Client-to-site VPN  

	- Clientless  
	
	- Split tunnel vs. full tunnel  
	
- Connection methods  

	- SSH  
	
	- Graphical user interface (GUI)  
	
	- API  
	
	- Console  
	
- Jump box/host  

- In-band vs. out-of-band management   


## 4.0 Network Security  

### 4.1 Explain the importance of basic network security concepts  

- Logical security  

	- Encryption  
	
		- Data in Transit  
		
		- Data at rest  
		
	- Certificates  
	
		- Public key Infrastructure (PKI)  
		
		- Self-signed  
		
	- Identity and access management (IAM)  
	
		- Authentication  
		
			- Multifactor authentication (MFA)  
			
			- Single Sign-on (SSO)  
			
			- Remote Authentication Dail-in User Service (RADIUS)  
			
			- LDAP  
			
			- Security Assertion Markup Language (SAML)  
			
			- Terminal Access Controller Access Control System Plus (TACKTS+)  
			
			- Time-based authentication  
			
			- Authorization  
			
				- Least Privilege  
				
				- Role-based access control  
				
			- Geofencing  
			
- Physical Security  

	- Camera  
	
	- Locks  
	
- Deception technologies  

	- Honeypot  
	
	- Honeynet  
	
- Common security terminology  

	- Risk  
	
	- Vulnerability  
	
	- Exploit  
	
	- Threat  
	
	- Confidentiality, Integrity, and Availability (CIA) Triad   
	
- Audits and regulatory compliance  

	- Data locality  
	
	- Payment Card Industry Data Security Standards (PCI DSS)  
	
	- General Data Protection Regulation (GDPR)  
	
- Network segmentation enforcement  

	- Internet of Things (IoT) and Industrial Internet of Things (IIoT)  
	
	- Supervisory control and data acquisition (SCADA)
	
	- Industrial Control System (ICS)  
	
	- Operational Technology (OT)  
	
	- Guest  
	
	- Bring your own device (BYOD)  
	

### 4.2 Summarize various types of attacks and their impact to the network  

- Denial-of-service (DoS) / Distributed denial-of-service (DDoS)  

- VLAN hopping  

- Media Access Control (MAC) Flooding  

- Address Resolution Protocol (ARP) poisoning  

- ARP spoofing  

- DNS poisoning  

- DNS Spoofing  

- Rogue device and sevices  

	- DHCP  
	
	- AP  
	
- Evil Twin  

- On-path attack  

- Social Engineering  

	- Phising  
	
	- Dumpster diving  
	
	- Shoulder Surfing  
	
	- Tailgating  
	
- Malware 


### 4.3 Given a scenario, apply network security features, defense techniques, and solutions  

- Device hardening  

	- Disable unused ports and services  
	
	- Change default passwords  
	
- Network access control (NAC)  

	- Port Security  
	
	- 802.1X 
	
	- MAC filtering  
	
- Key management  

- Security rules  

	- Access Control List (ACL)  
	
	- Uniform Resource Locator (URL)  
	
	- Content filtering  
	
- Zones  

	- Trusted vs. Untrusted  
	
	- Screened subnets  
	


## 5.0 Network Troubleshooting  

### 5.1 Explain the Troubleshooting methodology  

- Identify the problem  

	- Gather information  
	
	- Question Users  
	
	- Identify symptoms  
	
	- Determine if anything has changed  
	
	- Duplicate the problem, if possible  
	
	- Approach multiple problems idividually  
	
- Establish a theory of probable cause  

	 - Question the obvious  
	 
	 - Consider multiple approaches  
	 
		- Top-to-bottom/bottom-to-top OSI model  
		
		- Divide and conquer  
	
- Test the theory to determine the case  

	- If theory is confirmed, determine next steps to resolve problem  
	
	- If theory is not confirmed, establish a new theory or escalate  
	
- Establish a pain of action to resolve the problem and identify potential effects  

- Implement the solution or escalate as necessary  

- Verify full system functionality and implement preventive measures if applicable  

- Document findings, actions, outcomes, and lessons learned throughout the process  


### 5.2 Given a scenario, troubleshoot common cabling and physical interface issues  

- Cable issues  

	- Incorrect cable  
	
		- Single mode vs. multimode  
		
		- Category 5/6/7/8/  
		
		- Shielded twisted pair (STP) vs. unshielded twisted pair (UTP)  
		
	- Signal degredation  
	
		- Crosstalk  
		
		- Interference  
		
		- Attenuation  
		
	- Improper termination  
	
	- Transmitter (TX)/ Receiver (RX) transposed  

- Interface issues  

	- Increasing interface counters  
	
		- Cyclic redundancy check (CRC)  
		
		- Runts  
		
		- Giants  
		
		- Drops  
		
	- Port Status  
	
		- Error disabled  
		
		- Administrative down 
		
		- Suspended  
		
- Hardware issues  

	- Power over Ethernet (PoE)  
	
		- Power budget exceeded  
		
		- Incorrect standards  
		
	- Transceivers  
	
		- Mismatch  
		
		- Signal Strength  
		
		
### 5.3 Given a scenario, troubleshoot common issues with network services  

- Switching Issues  
	
	- STP  
	
		- Network loops  
		
		- Root bridge selection  
		
		- Port roles  
		
		- Port States  
		
	- Incorrect VLAN assignment  
	
	- ACLs  
	
- Route Selection  

	- Routing table  
	
	- Default routes  
	
- Address pool exhaustion  

- Incorrect default gateway  

- Incorrect IP address  
	
	- Duplicate IP address  
	
- Incorrect subnet mask  


### 5.4 Given a scenario, troubleshoot common performance issues  

- Congestion/contention  

- Bottlenecking  

- Bandwidth  

	- Throughput capacity  
	
- Latency  

- Packet loss  

- Jitter  

- Wireless  

	- Interference  
	
		- Channel overlap  
		
	- Signal degredation or loss  

	- Insufficient wireless coverage  
	
	- Client disassociation issues  
	
	- Roaming misconfiguration  
	
### 5.5 Given a scenario, use the appropriate tool or protocol to solve networking issues  

- Software tools  

	- Protocol analyzer  
	
	- Command line  
	
		- `ping` 
		
		- `traceroute`/`tracert`  
		
		- `nslookup`  
		
		- `tcdump`  
		
		- `dig`  
		
		- `netstat`  
		
		- `ip`/`ifconfig`/`ipconfig`  
		
		- `arp`  
		
	- Nmap  
	
	- Link Layer Discovery Protocol (LLDP)/ Cisco Discovery Protocol (CDP)  
	
	- Speed tester  
	
- Hardware tools  

	- Toner  
	
	- Cable tester 
	
	- Taps  
	
	- Wi-FI analyzer  
	
	- Visual fault locator  
	
- Basic networking device commands  

	- `show mac-address-table`  
	
	- `show route`  
	
	- `show interface`  
	
	- `show config`  
	
	- `show arp`  
	
	- `show vlan`  
	
	- `show power`  
	
			
		
	
	
	


