#### ESXi Update:
- Google ESXi patches `<# of version you have>`
- Website should be: [Esxi-patches.com](https://esxi-patches.v-front.de/)
- This site will give you commands to run the update.
- you will need to add `--no-hardware-warning`
- The command will take 5-15 minutes or more to run
- Example command:

```bash
esxcli software profile update -p ESXi-8.0U3-24022510-standard \ 
-d https://hostupdate.vmware.com/software/VUM/PRODUCTION/main/vmw-depot-index.xml --no-hardware-warning
