# Comptia A+ Core 1  

## Fundamentals  
* b means bit, B means bytes. 
	- So 200 Mbps = 200,000,000 bits per second
	- 4 MB = 4,000,000 B x 8 bits = 32,000,000 bits  
* **Throughput unit** 
	- Kbps, Mbps, Gbps, Tbps all per second    
* **Processing Speed**  
	- Frequency of electrical cycles per second
	- MHz, GHz  
* Devices  
	- The old mouse and keyboard connection to computers (round with pins) was called a PS2 connection  
	- CMOS = BIOS chip  
	- Chipset: directs the communication between the processor and rame  
* Storage types  
	- Local Network  
		- NAS - Network Attached Storage  
		- File Server 
		- Local Cloud
	- Remote Network  
		- Cloud 
## Mobile Devices  
**RTM** - read the manual. This is per device, for maintenance.  
* Digitizer - like a signing pad, takes a written representation and puts it into a digital format  

### Displays  
* LCD - Liquid Crystal Display  
	- It doesn't produce light  
	- Uses a backlight
		- Cold Cathode Fluorescent Lamp (CCFL)  
	- Inverter
		- Converts DC to AC for the backlight  
		- If there is a problem with flickering or dimness it might be the inverter  
	- Display technology 
		- Twisted nematic (TN)
			- very old
			- good response time  
			- very little lag, high refresh rate, 240 Hz  
			- Bad at angles  
		- In-plane switching (IPS)  
			- Great color  
			- Good view angles  
			- Little lag  
		- Vertical alignment (VA) 
			- Great Color  
			- Okay Response  
		- Organic light-emitting diode (OLED)
			- Light-emitting compound  
			- There is no need for a backlight 
				- Which means that it can have a dark black color  
			- Contrast ratio of OLED displays exceeds that of LCD  
			- OLED is highest quality  
			- Found in smaller devices  
### Device Accessories  
* Port replicator - reproduces the functions of the ports. (Looks like a usb hub to me)  
	- Will have usb, display (HDMI, DP, VGA), or ethernet connection
* Docking station - similar to port replicator but can have a full drive bay, optical drives, memory card slots  
* RAM
	- SODIMM - most laptops use Small Outline Dual in-line Memory Modules
### Connection methods  
* USB - universal serial bus
	- c / microUSB/ miniUSB  
* Bluetooth - 30ft range  
* NFC - 4cm range  
	
### Bluetooth and MDM 
* Mobile Device Management(MDM)/ Mobile Application Management (MAM)  

### Cellular Standards  
* xG - The G stands for generation  
* 2G - handle phone calls, SMS, and limited data
	- GSM (GLobal System for Mobile Communication)
		- used by AT&T and T-Mobile  
		- The US and the rest of the world used GSM
	- CDMA (Code-Driven multiple acces)  
		- used by Sprint and Verizon
		- Uses preferred roaming list (PRL)
			- Required contiunous updates with PRL to establish communications
	- GSM and CDMA were not compatible with eachother
* 3G - allows additional features such as mobile Internet access, video calls and modile TV  
* 4G 
	- WIMAX and Long-Term Evolution (LTE) where 2 standards, LTE won.  
	- Faster than 3G, Theoretical max is 300Mbps down and 75 Mbps Up.
	- No need for GSM or CDMA  
	- One standard  
* 5G
	- 100x faster than 4G  
	- May hit speeds of 20Gbps  
	- Low-latency links (Connects very fast between devices)
	
### Data Synchronization  


## Networking  
### Protocols  
* TCP/IP 
	- Made of many protocols like HTTP and FTP
* TCP - connection oriented Protocol  
	- In the applications and network layers of OSI
	- Keeps tract of the segments being transmitted or received by assigning numbers to every single one  
	- Flow control limits the rate of data transfer to ensure reliability  
	- It won't load the whole page if a single piece of the data is missing  
	- 24-60 bytes (high overhead)
* UDP - User Datagram Protocol, is connectionless and unreliable but fast  
	- Used for smaller data sized transfers
	- Suitable for milticasting and packet switching  
	- Used for real-time applications  
![alt text](./images/udp_tcp.JPG "missing udp_tcp.JPG")

### Ports  
* 65,535 ports on a computer  
* File Transfer Protocol - FTP
	- share files over a LAN or WAN  
	- TCP port 20 and 21  
	- Supports authentication, authorization, and directory browsing  
	- Unencrypted. Should use SFTP 
	- **FileZilla** application for FTP  
* Trivial File Transfer Protocol  
	- Used to push or pull files from a server  
	- Commonly used to manage devices like IP phones, routers, switches  
	- DOES NOT SUPPORT authentication, authorization, or diretory browsing  
	- UDP port 69  
	- Unencrypted, use SFTP
* Secure File Transfer Protocol  
	- Secure version of FTP  
	- has encryption  
	- SFTP is an extension of SSH which is shy they use the same port number  
	- TCP Port 22  
* Simple Mail Transfer Protocol  
	- outgoing mail to a server  
	- TCP Port 25  
* Post Office Protocol (POP3)  
	- Downloads incoming mail from server  
	- TCP port 110  
* Internet Message Access Protocol (IMAP)  
	- synchronizes incoming mail from a server  
	- TCP port 143  
* Telnet  
	- provides remote command line acces to interact with a server  
	- Considered insecure and should no longer be used, use SSH instead  
	- TCP port 23  
	- More common on Linux  
* SSH - Secure Shell 
	- provides encrypted remote command line access to interact with a server  
	- SSH Version 2 added SFTP and SCP support 
	- TCP port 22  
	- **PuTTY** is the application used  
* DNS 
	- TCP/UDP port 53  
* DHCP - Dynamic Host Configuration Protocol  
	- provides various configurations to clients in an IP network via broadcast  
	- UDP port 67 is the server port, and 68 is the client port  
* HTTP
	- TCP port 80
* HTTPS
	- securely transfers using SSL or TLS  
	- TCP port 443  
* NetBIOS  
	- Network Basic Input/Output System provides communications in Windows Network 
	- Used in Windows before IP networking  
	- NetBIOS over TCP/IP is still used in Windows  
	- TCP/UDP  port 137/139  
* SNMP - Simple Network Management Protocol
	- used to query, configure, and monitor host in LAN  
	- SNMPv3 encrypts communication where previous versions did not  
	- UDP port 161/162  
* LDAP - Lightweight Directory Access Protocol 
	- used in domain-based network environments to facilitate system and user management  
	- TCP/UDP port 389  
* Server Message Block (SMB)
	- file sharing, network browsing, print services  
	- Commonly used in Windows networks but supported in Linux and MacOS  
	- CIFS(Common Internet File System) is an open implementation used on Linux and macOS  
	- TCP port 445  
* RDP - Remote Desktop Protocol  
	- securely access Windows desktop  
	- TCP port 3389  
	
### TCP vs UDP  
* TCP  
	- TCP Segment  
		- 24-60 bytes  
![alt text](./images/tcp_segment.JPG "missing tcp_segment.JPG") 
		- Connection-oriented  
		- Virtual Circuit  
		- Sequenced  
* UDP segment  
![alt text](./images/udp_segment.JPG "missing udp_segment.JPG")  
	- 8 bytes, lightweight  
	- un-sequenced  
	- no virtual circuit  
	- connectionless  

### Networking Devices  
* NIC - Network Interface Card  
	- connect to the network  
	- each one has a 48-bit MAC address 
	- The link light and activity lights are used to troubleshoot connections made to the NIC  
		- **Link light** verifes the cable is plugged in. It is the light on the left.  
		- **Activity Light** will blink as data goes throught he interface  
* Hubs - not used anymore because it broadcast to every port.  There were data collisions 
* Switch 
	- replaces hub  
	- used to connect and manage wired communications in a LAN  
		- Forward frames based on MAC addresses  
		- Managed switch vs unmanaged switch  
			- Managed switches can be configured
				- used in enterprise LANs to meet their needs for enforcing policies  
				- Provide additional functions like VLANs, port security, DHCP snooping, and dynamic ARP inspection  
				- expensive  
			- Unmanaged switches cannot be configured  
				- used in SOHO networks  
				- Lower cost  
* Router 
	- used to connect different broadcast domains to eachother  
	- Commonly used to connect a LAN to a WAN (site to site or the Internet)  
	- Forwards traffice based on IP Address in packets  
	- Can usuall provide DHCP  
* Firewall
	- Security device used to prevent authorized access to a LAN from the Internet  
	- can be hardware appliance or host-based software  
* Access Point (AP)  
	- used to provide and manage wireless communications in a LAN 
	- Uses Radio Frequencies (RF) to transmit data to the host  
* SOHO Router (Small office, Home office)
	- multifunction device offering many features beyond routing  
	- Includes: wireless, switching, firewall, security, and DHCP  
	- Can include: content filtering, file server, print server, VPN client and server, and other features  
	- Forwards traffic based on IP Addresses in packets  
	
* Power over Ethernet (PoE)  
![alt text](./images/poe_chart.JPG "missing poe_chart.JPG")
	- Requires a dedicated PoE switch, or else you can use a PoE Injector  
	- Allows you to power devices using just an Ethernet cable 
* DSL - digital subscriber line  
	- used over telephone lines  
* ONT - Optical Network Terminal
	- converts optical signal from fiber  
* Software-defined networking (SND)  
	- SDN Controller in the control plane directs communications between devices in the data plane  

### Join wireless networks

### 2.4 GHZ vs 5 GHz  
* 2.4 GHz Spectrum  
	- Long range communication, better penetration through barriers
	- Slower than 5 GHz  
	- Higher rate of interference because of long range  
	- 11 channels in total  
	- Non-overlapping channels 1, 6, 11 offer the best chance of minimizing interference  
* 5 GHz Spectrum  
	- Short range, poor penetration  
	- Faster data rate  
	- 45 channels, 24 non-overlapping  
	- 20 MHz uses 36, 40, 44, 48, 149, 153, 157, 161, 165  
	- 40 MHz uses 38, 46, 151, 159  
	- Low chance of interference because of its shorter range  
	
### Wifi Standards  
* WIFI 4  and up supports MIMO (Multiple in, Multiple Out)  
![alt text](./images/wifi_standards.PNG "missing wifi_standards.PNG")  

### WIFI Considerations  
* SSID (sevice Set Identifier)  
	- name of the wifi network  
	- always change the default name  
* IP Address - set a static IP for administration  
* change default username and password  
* Long-Range fixed wireless  
	- used to connect wireless devices over miles  
	- Usually installed using point-to-point directional antennas  
	- May have to go to the FCC to et a license for the radio frequency  
* RFID (Radio-frequency identification) 
	- uses electromagnetic fields to automatically identify and track tags attached to objects  
	- used in access cards, ez-pass, or inventory management  

### Types of servers  
* DNS - translate domain name to IP address  
* DHCP - gives out IP address on a network  
* Fileshare - sshares files and folders on network  
* Print Servers  
* Mail Servers  
* Syslog - Recieves logs from devices in network  
* Web Servers  

### Internet Appliances  
* Spam Gateways - keeps spam from entering emails  
* Unified Threat Management (UTM)  
	- A combination of antimalware, firewall and intrusion detection system  
* Load Balancers - allow multiple servers served the same amount of traffic  
* Proxy Servers  
	- Request webpages on behalf of users  
	- Can be used to filter out web traffic, such as blocking users from seeing Facebook  
* SCADA (Supervisory control and data acquisition)  
	- Older utility systems such as providing gas and electric power  
	- May have to be sectioned off from the network to ensure no access  
	- Embedded/Legacy systems  

### Convert binary 
* Write out 8 bits  
* Put the 0 and 1 underneath each of the bits  
* 255 is the max of 8 bits  

### IPv4 address  
* IPv4 is 32 bits, 4 values of 255 max  
	- the first 8 bits can only go up to 223 (the far left one)  
* The IANA gives out blocks of IP addresses to ISPs

### Network Classes  
* the first 8 bits max at 223 because of class D an E below  
![alt text](./images/classful_ranges.PNG "missing classful_ranges.PNG")  


### Figuring out the Network ID  
Take the IP address, put it over the subnet mask. If the IP is above 255, use the IP number, if the subnet mask is 0, use the 0.  
- EX: IP = 192.168.30.10  
Subnet Mask = 255.255.255.0  
Network ID is = 192.168.30.0   
* Computers with the same Network ID are on the same switch (possibly) and can talk to eachother  
* Devices with different Network IDs will need a router to communicate  


