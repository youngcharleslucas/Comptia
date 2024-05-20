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





