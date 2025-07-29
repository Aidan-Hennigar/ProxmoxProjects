# ProxmoxProjects
An overview of my processes and setup of my Proxmox server, where I learn and play.

Remove the remains of what once was.

This setup began with troubleshooting an unknown setup of a donated Z840 workstation with 
dual Xeon ___, 8x4gb 2333 ecc ram, Nvidia quadro M6000, a hardware raid card, 4 1tb sas drives in raid, and 1 2tb sata drive.






***Overview***  
**Setup**  
*Boot drive*  
2tb drive for boot, container & VM config storage.   

*Bulk storage*  
RAIDZ ZFS pool, l4e compression.
4x 1tb drives, 3tb usable storage with 1 drive redundancy.  


**Media**  
Two Ubuntu 20.04 containers. 

*Media*
Hosts PLex server with auto pull script to change metadata from sandboxed Qbit download location...  

*Qbit*
Hosts Qbit webUI with Mullvad tunnel via WireGuard, preventing any dns leaks.


*07/15*
Windows server setup, absolute pain in the ass, server 2025 core. Could not install Word, switched to server W gui, couldn't just install word, had to do full office installation. Com integration and WSL are now set up in working order to run one of my projects. 
Basically started over, setting everything up much smoother, ZFS directories for things that we want to keep separate, nice network share container running samba that links to the three main zfs direcotries, general, photos, and mediarr.
Media services are now running on an Ubuntu server VM, connected to that network share. Everything is managed with Docker for easy updates and simplified networking.


*07/28*
Network change, had to fix network configs for new modem.
Completed revamp of my Media server
New Ubuntu container to manage Samba network shares as the main entry point to the ZFS pool.
New Ubuntu server VM with Docker to manage services
ARR apps are all hosted inside a Docker network with routing through Gluetun for privacy and security. 
