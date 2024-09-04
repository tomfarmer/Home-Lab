> [!Note]
> Below is a list of errors I have ran into when setting up Sec Onion, some of them are straight up error codes while others are descriptions of what was going wrong and how to fix it.


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

