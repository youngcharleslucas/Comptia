# A+ Part Deux  

## Operating Systems  

- Purposes  
	- File management  
	- Network Connection  
	- Security  
	
- Types: 
	- Closed Source: Windows, only available from one organization  
	- Open Source: Distributed by many organizations  

### Windows Upgrades  

- Must have a previous bootable version of Windows installed  
- Installation media on removable media or stored locally  
- Upgrade paths: 
	- 7 and 8.1 => 10 
		- 8.0 => 8.1 => 10
	- 10 => 11
	- pro 7 => 10  
		- going from professional to home will cause a loss of professional features.  
		- Pro connects to a domain and has more security  

### Windows 10  

- Released in 2015
- Supported until 2035  

| Component | 32-bit | 64-bit |  
| --- | --- | --- |  
| CPU | 1 GHz | 1 GHz |  
| RAM | 1 GB | 2 GB |  
| Storage | 16 GB | 32 GB |  
| Graphics | DirectX 9 or > | DirectX 9 or > |  

Versions:  

![10 home](./images/w10_home.png)  

![10 pro](./images/w10_pro.png)  

![10 enterprise](./images/w10_enterprise.png)  

### Copy Command  

- `copy` is used to copy files from one folder to another  
- `xcopy` can copy folders, subfolders, and all the files with them  
- `robocopy` is more advanced copy task than xcopy  

### Disk management commands  

- `chkdsk` scans a disk in hopes fo recovering corrupted files  
	- `/f` fixes errors on the disk  
	- `/r` fixes error and locates bad sectors  
- `format` erases a disk file applying a file system  
	- `/fs` specifies the type of the file system (FAT, FAT32, exFATE, NTFS)  
		- `format d: /fs:ntfs` will format the D drive as ntfs  
	- `/q` performs a quick format  
		- `format d: /fs:fat32 /q` performs a quick format on the D drive as fat32  
- `convert` changes FAT/FAT32 filesystem to NTFS without erasing files  
	- `/fs` specifies that the volume will be converted to NTFS.
	- **Cannot convert NTFS to any other file system**  
- `diskpart` is a command line partition managemnt tool  

### CMD commands  

- `/?` shows help on a command  
- `cd` or `chdir`  
- `md` or `mkdir`  
- `rd` or `rmdir` 
	- only deletes **Empty** folders  
- `del` delete file  
- `tree`  
- Drive navigation with `C:`  
- `winver` shows windows version  
- `cls` clear screen  

### Network Commands  

- `net use` used to connect to a network share  
	- `net use x: \\servername\sharename`  
	- EX: Add a shared folder, called 'R:'  
	- Create a folder on a host computer, your computer for this. 
	- Right click and folder, go to Sharing // Advanced Sharing, grant permissions to everyone if you want  
		- This will share the folder on the network  
	- Check your hostname with `hostname`  
	- Window key type in `run` 
	- type in `\\hostName`. This will show the shared folder  
	- Give it a drive name with `net use r: \\hostName\sharedFolder`  
	
- `netstat` displays active network connections  
	- `-a` displays all connections, including listening ports  
- `tracert` uses ICMP to return a hop count  
- `net user` used to manage user accounts 
	- `net user userName password /add`
- `pathping` performs a ping and a traceroute at the same time  
- `nslookup` identifies the current DNS server and displays IP Addresses for a provided name  
- `hostname` displays a computer's hostname   

- `ping` uses ICMP to return the status of a unicast  
	- `-n` changes the number of pings sent  
	- `-l` changes the size of the ping packet  
	- `-t` pings continuously  
	- `-4` force an IPv4 ping  
	- `-6` force an IPv6 ping  
	
- `ipconfig` Displays ingerface configurations  
	- `/all` displays more detailed information  
	- `/renew` request configurations from a DHCP server  
	- `/release` removes configurations obtained through DHCP  
	- `/displaydns` displays the local DNS cache  
	- `/flushdns` clears the local DNS cache  

### Disk Tools and the registry  

- Disk Cleanup (clanmgr.exe)  
	- Files in teh Recycle Bin  
	- Temporary Internet files  
	- Downloaded program files  
	- Temporary files  

- Disk Defragment (dfrgui.exe)  
	- Optimize and Defragment Drives (Windows 10)  
	- Defragmenting (HDD) - Bits on a hard disk drive are rearranged so files can be loaded faster.  
		- Defragging a drive too frequently can decrease its lifespan  
	- Trimming (SSD)  
		- Makes sure that the NAND memory chips on an SSD ar worn evenly to mazimize the lifespan of the drive  

- Registry Editor (regedit.exe)  
	- a database that stores all the settings and configurations for Windows and it's appliaitons  
	- the `regedit` command can be used to launch the Registry Editor  
- Registry Keys  
	- HKEY_CLASSES_ROOT: stores file association information  
	- HKEY_USERS: Stores settings that apply to all users  
	- HKEY_CURRENT_USER: Stores settings for he individual users  
	- HKEY_LOCAL_MACHINE: Stores settings for all devices that have been installed or removed form the system  
	- HKEY_CURRENT_CONFIG: Stores settings for individual devices when multiple of the same type of device have been installed  

### Event Viewer (eventvwr.msc)  

Displays logs of timestamped events which can be used to assist with troubleshooting  

- Windows Logs  
	- System: list operating system events  
	- Security: list security events  
	- Application: list application events  
	
- Icons  
	- Red = Error  
	- Yellow = Warning  
	- White = Informational  
	
### Microsoft Managment Console (mmc)  

Put all the management tools in one place.  
Create a custom toolbox of useful utilities referred to as "Snap-ins"  

- Snap-ins are the other consoles that are available elsewhere like the Device Manager or Disk Management  
- `mmc` command can be used to launch the Microsoft Management Console  

- Useful Snap-ins  
	- Disk Management (diskmagmt.msc)  
		- Manage Disk Partitions
	- TaskScheduler (taskschd.msc)
		- Create and schedule tasks to run
	- Device Manager (devmgmt.msc)  
		- Check, update and install device drivers
	- Certified Manager (certmgr.msc)
		- Check and manage certificates installed on a computer
	- Local Users and Groups (lusrmgr.msc)  
		- Create, change and delete users on local computer  
	- Performance Monitor ( perfmon.msc)  
		- Monitor computer performance  
	- Group Policy Editor (gpedit.msc)  
		- Edit local group policy  
	

### System info and Configuration  

System information is for viewing detailed information on system hardware and software  

- `msinfo32` command can be used to launch the System Information utility  
	- Hardware Resources : identify hardware conflicts and addresses  
	- Components: Identify driver details and hardware capabilities  
	- Software Environment: Identify software details  
	
- `msconfig.exe` System Configuration  
	- General: change startup type between Nromal, Selective, or Diagnostic types  
	- Boot: change multiboot order  
	- Services: Enable or disable services  
	- Startup: Links ro the Startup tab in the task manager  
	- Tools: Collection of useful tools  

### Task Manager  

- Processes: 
	- Displays all running processes including background processes  
	- Non-responsive processes can be closed here  
- Performance: Displays performance graphs  
- Users:
	- Displays currently logged-in users  
	- It is possible to log out users in this tab  
- Startup: Disable or enable auto-starting applications  
- `taskmgr` can be used to launch the task manager via a run box  
- Ctrl + Shift + Esc

### Control Panel Options  

Filled with applets  
This covers Windows 10 Control Panel utility  

- Internet Options  
	- Configure default internet browser options  
- Devices and Printers  
	- Add, remove, and administrate printers, scanners, cameras, etc.  
- Programs and Features  
	- Reinstall, uninstall programs and windows features  
- Network and Sharing Center  
	- Check and administer NIC  
- System  
	- Check computer specification, rename computer, join domain or workgroup  
- Windows Defender Firewall
	- Check and change firewall setting. Can open ports.  
- Mail  
	- Add, remove, or repair mailboces. Mostly used by Microsoft Outlook.  
- Sound  
	- Use to setup speaker or mic's on a computer  
- User Accounts  
	- Use to change, add, or remove local user accounts  
- Device Manager  
	- Check if devices are functioning correctly. Update or rollback drivers.
- Indexing Options   
	- Check what is being index on a system  
- Administrative Tools  
	- Set of commonly used utilities to manage the system  
- Ease of Access 
	- Make the system easier to use for persons with disabilities  
- File explorer Options  
	- Show hidden files  
	- Hide extensions  
	- General options  
	- View options  
- Power Options  
	- Hibernate  
	- Power Plans  
	- Sleep/suspend  
	- Standby  
	- Choose what closing the lid does  
	- Turn on fast startup  
	- Universl Serial Bus (USB) selective suspend   

**Hibernate** takes everything on the RAM and stores it on the hard drive  
**Sleep Mode** puts the computer in a very low power mode  


### App Settings  
- Time and Language  
	- Configure time and date, and language used on the computer.  
- Update and Security  
	- Set when updates will be applied to the computer  
- Personalization  
	- Personalization of the system to the user likening such as background 
- Apps  
	- Uninstall applications, change window defaults, and enable or disable windows features  
- Privacy  
	- Set what can be tracked on the system  
- System  
	- Allows you to change display information, sound, and notification setting  
- Devices  
	- Manage Bluetooth, printers, and a mouse  
- Network and internet  
	- Manage and connect new NIC 
- Gaming  
	- Connect Xbox gaming accounts  
- Accounts  
	- Create and link new accounts to the system  
	
### Firewall  

- Block all incoming traffic  
- Allows all outgoing traffic  
- Configure and manage with rules  
- Will need to make an exception to allow certain traffic such as ftp through the firewall  
- Access by searching `Defender`  

### Network Configurations  

- Internet PRotocol addressing scheme  
- DNS settings  
- Subnet mask  
- Gateway  
- Static vs Dynamic  
	- Static is manually typed in by a tchnician, Dynamic is assigned by the DHCP  
	- If no DHCP is available when selecting dynamic, the computer will APIPA address of 169.254.x.x  
- WWAN ( Wireless sidae area network)  
	- Internet access using a wireless connection. Done by using an adapter form a mobile cellular network using tchnologies such as 4G or 5G.  
- Private vs Public Network  
	- When connecting to WIFI, your computer will ask if this is Public or Private. 
	If the WIFI is public, the computer will block sharing and discovery from other computers. 
	Increased security  
- Metered Connection  
	- ISP limits the amount of data allowed. 
	You can tell your computer to not exceed the limit.  
	
### Shared Resources  

Folders and devices shared on network  
- Printers  
- File servers 
- Shared Network Folders 
- Mapped Drives  
	- Allows a shared folder on another computer to act as a drive on a system  
	- Share the folder as a shared Network folder first. Then set it as a drive.  
	
### Workgroup vs Domain  

Workgroup  
	- Decentralized setup used in SOHO  
	- Uses local user accounts  
	- **No central server** for computer or user management  
	- Simple to setup with no additional server software needed.  

Domain  
	- Centralized setup used in small-large businesses  
	- User accounts are **managed on a central server** called <u>domain controllers</u>  
	- Computer configuration and security setting are set on a central server  
	- Need to setup a server (Windows Server), more expensive  
	- Adding a user ( and computer) to a domain
		- In the server active directory, when looking at users, they are stored in Organizational Units, not folders, for a Group 
		- In the server, create a new user  
		- In the computer you wan to connect to the domain, an administrator must use their credentials to add the computer from that computer.  
			- Control Panel > System and Security > Settings > Advanced System Settings > Rename or change computer domain
		- Now someone can log in as the user that was created on the server  
	
### Installing Applications  

- 32-Bit vs 64-Bit Requirements  
	- 64 bit processors can handle large amounts of RAM vs 32-bit  
	- 32-bit can use 4GB of RAM  
	- 64-Bit can use 16 exabytes of RAM  

- Requirements when installing Applications  
	- Dedicated graphics vs integrated  
		- some applications will require high end graphics  
		- VRAM (Video random-access memory )  
			- Memory built in the graphics card  
	- RAM  
	- CPU  
	- Hardware token
		- For secuirty, device will require a usb stick with a token to be inserted inorder to boot up  
- Distribution methods  
	- Physical media vs Downloadable  
	- ISO mountable 
		- ISO are a direct copy of an optical disk without compression  
		- image of a disk  
		- single file that stores all the necessary files for the application  
		
### File Systems  

**Windows File Systems**

FAT32 (File Allocation Table 32)  
- Advantage:
	- Most compatible file system  
- Disadvantage  
	- Partitions are limited to 32GB  
	- Files are limited to 4GB  
	- No security features  

NTFS (New Technology File System)  
- Advantages  
	- Supports partitions bigger than 32GB  
	- Supports files bigger than 4GB  
	- Disk quotas  
	- File and folder compression  
	- File system security  
		- File and folder permission  
		- EFS (Encryption file system)  
- Disadvantage  
	- Only officially compatible with Windows  

exFAT (Extensible FAT)  
- Advantage  
	- More compatible than NTFS  
	- Supports partitions bigger than 32GB  
	- Supports files bigger than 4GB  
- Disadvantage  
	- No security features  
	
**Non-Windows File Systems**  

- macOS File Systems 
	- HFS+ (Hierarchical File System Plus)  
	- APFS (Apple File System )  
	- macOS does support read and write access to FAT32 and exFAT partitions but only support read-only access to NTFS  
- Linux Files Systems  
	- ext3: (Third Extended File System)  
	- ext4: ( Fourth Extended File System)  
	- Linux can read and write to NTFS, FAT32, exFAT, and HFS+  
- Optical Disc Files System  
	- CDFS (Compact Dixc File System)  
	- UDF ( Universal Disc Format)  

![File System Compatibility](./images/file_compat.JPG)  

### Making a bootable USB Stick  

- Download the downloadable media from Windows site  
- Plug in a USB stick  
- Go through the installation process on the USB  

- **ISO** is used for Virtual machine installation  

- To install on the computer, change the boot order to boot into the USB  
- You can do this same process for repairing Windows, just select repair drive instead of install new  


### Installing an OS  

- Network  
	- Windows Deployment Service (WDS)  
	- Target computer must support network booting, 
	PXE (Preboot Execution Environment)  
		- Looks for the deployment server  

- Clean Installation  
	- Empty hard drive  
	- Bootable installation media  

- Cloning / Imaging (Ghosting)  
	- Duplicates the entire software installation of a system. Including the OS, drivers, applications, and configurations  
	- Can be done directly connected to the hard drive or over the network  
	- Before you clone the drive, you must run "SysPrep" to remove security IDs that are generated for activation purposes  
	
- Recovery Partition Installation (Similar to an Image)  
	- Pre-Built system sold with an OS already installed will either include a recovery partition with the OS, dirver, and other bundled software  
	- Returns computer to OEM, wipes drives
- Repair Installation  
	- Used to reinstall Windows files if the OS is giving issues  
- Third-Party Drivers  


### Partition Table Formats  

Logical segmenation of a physical hard drive  
Created for data separation  
- MBR (Master Boot Record)(old)  
	- This is the first sector of a MBR partitioned drive and contains code that informs the system about installed OS  
	- Allows 4 primaty partitions  
	- Limited to 2.2 TB partitions 
- GPT (GUID Partition Table)  
	- Theoretically allows for unlimited primary partitions  
	- Windows is limited to 128 primary partitions by design  
	- NOT limited to 2.2 TB partitions  
- Primary Partitions  
	- These partitions are used to boot an operating system.  
	- If you have multiple OS on one disk they each will require their own primary partitions  
- Extended Partitions  
	- These partitions are used to overcome the four primary partition limit  
	- A single extended partition can contain many logical drives, each logical drive appears as a partition but can not be used to store the OS.  
- Hidden Partition  
	- Often used by OEMs to store system recovery data (recovery partitions)  
- Swap partition  
	- Used a virtual memory by some OS  
- Drive Format  
	- Full Format  
		- Runs an additional step that checks the hard drive for any bad sectors  
	- Quick Format  
		- Drive is not checked for bad sectors  




