---
page_type: sample
languages:
- azurecli
products:
- azure-load-balancer
description: "Set up a virtual network with two virtual machines and a load balancer."
urlFragment: "https://github.com/MicrosoftDocs/mslearn-host-domain-azure-dns"
---

# Official Microsoft Sample

<!-- 
Guidelines on README format: https://review.docs.microsoft.com/help/onboard/admin/samples/concepts/readme-template?branch=master

Guidance on onboarding samples to docs.microsoft.com/samples: https://review.docs.microsoft.com/help/onboard/admin/samples/process/onboarding?branch=master

Taxonomies for products and languages: https://review.docs.microsoft.com/new-hope/information-architecture/metadata/taxonomies?branch=master
-->

Set up a load balancer to use in learn module exercise for "Host your domain on Azure DNS". Script creates:
- Virtual network for the VMs
- Network security group
- Two network interfaces
- Availability set
- Two virtual machines from a template
- Public IP address
- Load balancer
- Load balancer probe
- Load balancer rule

The script also:
- Updates the two network interfaces to associate them with the load balancer.
- Displays the IP address for the load balancer.


## Contents



| File/folder       | Description                                |
|-------------------|--------------------------------------------|
| `.gitignore`      | Define what to ignore at commit time     |
| `CODE_Of_CONDUCT.md` | Microsoft Open Source Code of Conduct |
| `LICENSE`         | The license for the sample               |
| `README.md`       | This README file.                          |
| `SECURITY.md`       | Security statement for Microsoft-owned repositories                         |
|`cloud-init.txt`             |Cloud-init script to configure the virtual machines     |
|`setup.sh`             | Script to set up and deploy a load balancer in Azure CLI                        |

## Prerequisites

The script is intended to be run from a BASH prompt in Azure Cloud Shell.

## Setup

At the start of the Microsoft Learn module exercise, run `bash src/setup.sh` to build the load balancer, virtual machines, and virtual network.

## Running the sample

To run the set-up script, run the following commands in Azure Cloud Shell:

  ```bash
  cd mslearn-host-domain-azure-dns  
  chmod +x setup.sh  
  ./setup.sh
  ```

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
