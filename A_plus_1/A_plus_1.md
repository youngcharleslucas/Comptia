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
* UDP - User Datagram Protocol, is connectionless and unreliable but fast  
![alt text](./images/udp_tcp.JPG "missing udp_tcp.JPG")

### Ports  
* 65,535 ports on a computer  
* File Transfer Protocol - FTP
	- share files over a LAN or WAN  
	- TCP port 20 and 21  
	- Supports authentication, authorization, and directory browsing  
	- Unencrypted. Should use SFTP  
* Trivial File Transfer Protocol  
	- Used to push or pull files from a server  
	- Commonly used to manage devices like IP phones, routers, switches  
	- DOES NOT SUPPORT authentication, authorization, or diretory browsing  
	- UDP port 69  
	- Unencrypted, use SFTP
	