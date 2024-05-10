# Azure VPN Lab with ASAv with BGP

This is the same setup and the other VPN lab but uses BGP instead of static routes.

This creates an onprem vnet with Cisco ASAv connected to a hub vnet vpn gateway and a spoke vnet attached to the hub. VM's are created in all 3 vnets. You'll be prompted for the resource group name, location where you want the resources created, your public ip, and username and password to use for the VM's and NVA. NSG's are placed on the default subnets of each vnet allowing RDP access from your public ip. This also creates a logic app that will delete the resource group in 24hrs. The topology will look something like this:

![vpnlab-asav](https://github.com/quiveringbacon/AzurevpnlabwithASAv/assets/128983862/1e379d69-6f6d-4dd5-819f-63d6cc443cfa)


You can run Terraform right from the Azure cloud shell by cloning this git repository with "git clone  https://github.com/quiveringbacon/AzureVPNLabwithASAv-withBGP.git ./terraform".
Then, "cd terraform" then, "terraform init" and finally "terraform apply -auto-approve" to deploy.

