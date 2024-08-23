**



ESXI:

ESXI Update:

Google esxi patches <#of version you have>

Website should be:

Esxi-patches.com

Will give you commands to run update

[https://esxi-patches.v-front.de/  
](https://esxi-patches.v-front.de/)You will need to add --no-hardware-warning to the main command, example below

esxcli software profile update -p ESXi-8.0U3-24022510-standard \ -d https://hostupdate.vmware.com/software/VUM/PRODUCTION/main/vmw-depot-index.xml --no-hardware-warning

Main command will take 5-15 minutes 

  

ESXI Shutdown:

The link is to an ESXI shutdown script, installing the scripts in the datastore will make them persistent, don't worry about the error saying it will not.  
[https://github.com/ThisIsTenou/esxidown/blob/master/esxidown.sh](https://github.com/ThisIsTenou/esxidown/blob/master/esxidown.sh)

  
**