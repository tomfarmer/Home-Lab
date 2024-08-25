Below is the link on how to setup VM Customization Specifications for windows and Ubuntu VMs. You can use this launch vms quicker and edit the ip address and more from the vm setup wizard.

Link to setting up: [VM Customization Specifications](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-EB5F090E-723C-4470-B640-50B35D1EC016.html)

### Ubuntu VM:
#### Ubuntu ISO Setup Script:
- Not sure how to sue this really
- Link: [Ubuntu ISO Setup Script](https://gist.github.com/wildactual/7cc9805dc7fa52d3aba6bbc69d6bbb0f)
#### Ubuntu VM Template Setup:
FORGOT IF THIS WAS FOR THIS OR TERRAFORM
1. Edit the VM boot time to be `10000`.
2. Hold `Shift` and keep clicking into the VMware remote console until you reach the "Press a button" page.
3. Select `F2`.
4. Change the hard drive to be the first option in the boot order.
5. Exit and save, then hold `Shift` again.
6. Select the second option that says “<something>(recovery Mode)”.
7. Then select `root Drop to root shell prompt`.
 **![Screenshot of Drop to root shell](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcS-Foxh4IP66EQkVHfYnZ_dki7KJ9jgE_2sPFjfObfgugbgQ1k_xB0yOQluhaWI9tuz_hk8v2Enko43dCga2_0Px3NzjhQT5lnaKKyYSuDXRhzzafAdgmeSFEAV0m9OB4Omgu0SATg1ymPXHPxB6noi6ms?key=656RGyT2tZdUq0NkJwJfuw)**
8. Press `Enter` to enter maintenance mode. 
9. Type the following command: ```bash dpkg-reconfigure cloud-init ``` 
10. Deselect all the options except `VMware` and `None`.
**![Screenshot Maintenance mode](https://lh7-rt.googleusercontent.com/docsz/AD_4nXebE1R9GkOSRhKA09xx6EbOLkDOGvIfgyk4BogPEm2t76n2r2F_Yn7rRsftjAuIUbk8DmuwnnQc_uBI6hPsdoA63vl9hKZsSRGzhqletOlSJmrIKejNppuLEb0-p2k7GaNxQtb-otU0sbc44PxKSdr7wm6U?key=656RGyT2tZdUq0NkJwJfuw)**
12. Type the following command:

    ```bash
    dpkg-reconfigure cloud-init
    ```

10. Deselect all the options except `VMware` and `None`.
11. Type the following commands:

    ```bash
    cloud-init clean
    shutdown -h now
    ```

