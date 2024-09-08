
To setup Security Onion, follow the ????. I provided **24 GB of RAM**, **8 CPUs**, and **1 TB of SSD/Hard drive space**. I also set up the Security Onion Manager and then the sensor, both with the same number of resources. I think I could have done with significantly less SSD space.

# Sec Onion Sensor Virtual Setup
Below is the link on the theoretical idea on one way to set up the Security Onion Sensor virtually
[How to Tap Traffic in a Virtual Environment](https://www.garlandtechnology.com/blog/design-it-how-to-tap-traffic-in-a-virtual-environment)

## VSwitch Setup

You are going to make two VSwitches:

1. **VSwitch Purple-Range-MGMT**: Contains Splunk and the Security Onion Manager.
2. **VSwitch Purple-Range**: Holds the Security Onion Sensor.

The Security Onion sensor will have:
- Its management NIC on the **VSwitch Purple-Range-MGMT**.
- Its sensor (ingest/bond) NIC on the **VSwitch Purple-Range**.

## Documentation

Make sure to read the current setup documentation for Security Onion. If you are setting up Security Onion in ESXi, follow their ESXi setup guide.  
[ESXi Setup Guide](https://docs.securityonion.net/en/latest/virtualbox.html)

Ensure you meet the minimum requirements for the sensor, manager, search head, etc.  
[Hardware Requirements](https://docs.securityonion.net/en/latest/hardware.html#hardware)

To better understand the setup of Security Onion, refer to the setup documentation:  
[Architecture Documentation](https://docs.securityonion.net/en/2.4/architecture.html)
