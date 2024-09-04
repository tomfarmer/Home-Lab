
#### VCSA Needing DNS:
> [!WARNING]
> In order for VCSA to work you need to have some form of DNS setup. You do not need full internet access just somewhere for VCSA to send the DNS packet.

### VCSA Setup:
1) Download VCSA from [vmware](https://knowledge.broadcom.com/external/article?articleId=366685) follow the steps provided on the website.		
> [!WARNING] 
> VCSA must be a version equal to or higher than the ESXI you are running.
2) One you have VCSA downloaded and unzipped it open the folder that was unzipped ex: `VCSA 8.0` 
3) Select `vcsa-ui-installer`
> [!NOTE]
> `vcsa-cli-installer` is used to install VCSA via the command line, I find it much harder than using the ui (user interface).
4) Select the folder for the operating system you are using, I normally only have success using the ui on windows machines.
5) select `installer.exe`
![](Images/Screenshot%202024-09-04%20at%2018.13.40.png)
7) A popup should appear and select `Install`
	A) There will be 2 parts. Part 1 will ask for your ESXI credentials and such and will log into the ESXI you give it and create the VCSA vm. Part 2 will show up automatically once Part 1 is finished, it will ask for more configuration information for VCSA. 
	B) When asked deployment size select tiny
	C) **DO NOT ENTER A FQDN.** For some reason when you input a FQDN you get a lot of problems.
	
> [!INFO]
> 

