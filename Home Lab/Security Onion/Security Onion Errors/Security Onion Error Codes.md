# Security Onion Error Codes
> [!Note]
> Below is a list of errors I have ran into when setting up Sec Onion, some of them are straight up error codes while others are descriptions of what was going wrong and how to fix it.

---
## IPTables-dropped
**Description:**
IPTables down and no traffic seen in Security Onion or Elastic at all. You can also suppress the errors that are coming to your console by following Resolution 2.

**Error:**
`IPTables-dropped: IN=ens192 (more data like MAC address)`

**Resolution 1:**
Go to the VSwitch where you have the management interfaces and turn off Promiscuous mode. It should be set to reject. This solves the no data issue but does not solve the IPTables problem.
Link: [Resolution1](https://security.stackexchange.com/questions/176487/security-onion-vmware-openwrt-iptables-mirroring)

**Resolution 2:**
1) Edit the `/etc/sysctl.conf` file:
```bash
sudo nano /etc/sysctl.conf
```

2) Add the following line to reduce kernel messages sent to the console:
	A) This setting controls the log levels that are printed to the console. The first number is the most important one, which you can set to 3 to show only critical kernel messages.
```bash
kernel.printk = 3 4 1 3
```
3) Validate the changes:
```bash
sudo sysctl -p
```
---
## Sensor Not Sending Data

**Description:**
Sec Onion sensor not sending data to the manager
**Error:** 
no data
**Resolution:**
you are using the wrong OS and version for sec onion. You need to reset everything up and select the correct version, right now Sec Onion 2.4 is using linux and Oracle Linux 9.x
**Links:** 
[Sec Onion 2.4 Base OS](https://docs.securityonion.net/en/latest/virtualbox.html)

---

## Sensor Not Gathering Data from Vswitch

**Description:**
Sec Onion sensor not gathering network traffic on all ports
**Error:**
No data on promiscuous port 
**Resolution:**
You need to make sure ESXI has a “mirror” and “vlan 4095” selected/on and “MAC address changes” to allow all multiple sensors NICs.
**Links:** 
[Sec Onion on Vswitch](https://github.com/Security-Onion-Solutions/securityonion/discussions/7185)**

---

