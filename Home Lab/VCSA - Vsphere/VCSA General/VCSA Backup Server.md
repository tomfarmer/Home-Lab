To send VCSA backup configurations to another server you to go to your vcsa servers management interface. Type your vcsa ip into the browser and add the port number 5480.
`vcsaserver-ip-address:5480`


1) On the left hand side you will see backup Server, select Backup Server
2) When filling out the information use the line below as an example to send the configuration file over ftp.
```bash
sftp://10.69.10.11:22/mnt/sdb/vcsa-backups
```

Below is the link to help guide you:
[VCSA Backup Server](https://docs.vmware.com/en/VMware-vSphere/6.5/com.vmware.vsphere.install.doc/GUID-8C9D5260-291C-44EB-A79C-BFFF506F2216.html)

