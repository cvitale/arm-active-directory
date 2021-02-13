# Create a new Active Directory lab on Azure VM

This template will deploy a new *cheap* VM, inside a new vNet. Based on original template, I leave a Public Load Balancer in front of the VM as entrypoint for the lab. You can add other VMs behing the NAT with ease.

Changes to reduce costs and to fit to my needs:
- unmanaged disks
- B-series VM (Standard_B2ms)
- reduced parameters
- added a Network Security Group to limit access to 3389

**ATTENTION: the NSG has a rule to allow 3389 from anywhere!!! I suggest to fix access to your IP, at least, or adopt proper security measures (VPN, JIT, Bastion, etc.).**



Click the button below to deploy

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fcvitale%2Farm-active-directory%2Fmaster%2Fazuredeploy.json)  [![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](https://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fcvitale%2Farm-active-directory%2Fmaster%2Fazuredeploy.json)

## Credits
Simon Davis
https://azure.microsoft.com/it-it/resources/templates/active-directory-new-domain/