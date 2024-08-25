### Link Used To Learn Terraform:
- [Creating VMs for Kubernetes Using Terraform and VMware vSphere](https://perdue.dev/creating-vms-for-kubernetes-using-terraform-and-vmware-vsphere/#creating-a-template-virtual-machine)

### To Launch Terraform:
*Note: This needs to be run from the Terraform directory with the `.tfvars` file in it.*

```bash
terraform apply --var-file=/Users/Tomcondon/homelab/terraform/env/mgmt/terraform.tfvars
```

### To Destroy VMs:
Note: This will not destroy everything, just the VMs listed.
```Bash
terraform destroy --var-file=/Users/<username>/homelab/terraform/env/mgmt/terraform.tfvars
```

### Adding Passwords to Launch Ubuntu VMs:
When launching VMs in Terraform you might not have added a username and password

Type the following command:
```bash
sudo passwd <username>
```
**![Screenshot Ubuntu change password](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdNKUnLR-ooooo8p9a3bqaeIcNTNGM0J3gQFo6i34LC3_168T0V2r3eajLsGzUJD21sQAILgAe2UJhgQJhzURZKYd7-mBQOgVMjiOBYE8cACmdH8y4F7LNQWY5n_Lcv6H5wGOqji3nnAcXzkDJxMrHXI9Y1?key=656RGyT2tZdUq0NkJwJfuw)**


