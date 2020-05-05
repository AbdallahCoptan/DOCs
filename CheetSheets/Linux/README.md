![Preview](./linux.png)

#### Table Of Contents

**[Linux command cheat sheet](#Linux-command-cheat-sheet)**

- [System](#System)
- [Hardware](#Hardware)
- [Users](#Users)
- [File Commands](#FileCommands)
- [Process Related](#ProcessRelated)
- [File Permission](#FilePermission)
- [Network](#Network)
- [Compression & Archives](#Compression-Archives)
- [Install Packages](#Install-Packages)
- [Install Source](#Install-Source)
- [Search](#Search)
- [Login](#Login)
- [File Transfer](#File-Transfer)
- [Directory Traverse](#Directory-Traverse)
---

In the Linux cheat sheet Commands are categorized into different sections according to its usage. We have designed the command in white color with black background as we often use on Linux shell. 

## System
| Command           	| Description                                                       	|
|-------------------	|-------------------------------------------------------------------	|
| `uname`            	|  Displays  Linux system information                                  	|
| `uname -r`         	| Displays  kernel release information                                 	|
| `uptime`           	| Displays how long the system has been running including load average 	|
| `hostname`         	| Shows the system hostname                                            	|
| `hostname -i`      	| Displays the IP address of the system                                	|
| `last reboot`      	| Shows system reboot history                                          	|
| `date`             	| Displays current system date and time                                	|
| `timedatectl`      	| Query and change the System clock                                    	|
| `cal`              	| Displays the current calendar month and day                          	|
| `w`                	| Displays currently  logged in users in the system                    	|
| `whoami`           	| Displays who you are logged in as                                    	|
| `finger username` 	| Displays information about the user                                  	|

## Hardware

| Command      				      	| Description                              			                         	|
|-------------------------------	|---------------------------------------------------------------------------	|
| `dmesg`                       	| Displays bootup messages                                                     	|
| `cat /proc/cpuinfo`           	| Displays more information about CPU e.g model, model name, cores, vendor id  	|
| `cat /proc/meminfo`           	| Displays more information about hardware memory e.g. Total and Free memory   	|
| `lshw`                        	| Displays information about system's hardware configuration                   	|
| `lsblk`                       	| Displays block devices related information                                   	|
| `free -m`                     	| Displays free and used memory in the system (-m flag indicates memory in MB) 	|
| `lspci -tv`                   	| Displays PCI devices in a tree-like diagram                                  	|
| `lsusb -tv`                   	| Displays USB devices in a tree-like diagram                                  	|
| `dmidecode`                   	| Displays hardware information from the BIOS                                  	|
| `hdparm -i /dev/xda`          	| Displays information about disk data                                         	|
| `hdparm -tT /dev/xda <:code>` 	| Conducts a read speed test on device xda                                     	|
| `badblocks -s /dev/xda`       	| Tests  for unreadable blocks on disk                                         	|

## Users

| Command           	| Description                                                       	|
|-------------------	|-------------------------------------------------------------------	|
| `id`                	| Displays the details of the active user e.g. uid, gid, and groups 	|
| `last`              	| Shows the last logins in the system                               	|
| `who`               	| Shows who is logged in to the system                              	|
| `groupadd "admin"`  	| Adds the group 'admin'                                            	|
| `adduser "Sam"`     	|  Adds user Sam                                                    	|
| `userdel "Sam"`     	| Deletes user Sam                                                  	|
| `usermod`           	| Used for changing / modifying user information                    	|
