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





