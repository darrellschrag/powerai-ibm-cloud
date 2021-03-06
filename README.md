# IBM PowerAI on IBM Cloud

This terraform template creates a GPU-based Power virtual machine in an IBM Cloud VPC. Once the VM is provisioned, GPU support and the PowerAI libraries are installed and a Tensorflow python example is run.

## License Agreement
By deploying this terraform template via IBM Cloud Schematics or via Terraform, you accept the Terms and Conditions of the [IBM License Agreement for Evaluation of Programs](https://www14.software.ibm.com/cgi-bin/weblap/lap.pl?li_formnum=L-CKIE-BL45W3).  If you do not agree to these terms, do not deploy this template.

## Deployment Architecture

This provisions a GPU-based Power virtual machine in an IBM Cloud VPC. Once the VM is provisioned, GPU support and the PowerAI libraries are installed and a Tensorflow python example is run. The intent is to show you can automate the creation of a powerful VM environment, execute a machine learning exercise, and tear down the environment.

More specifically, it creates the following resources:

* a Virtual Private Cloud (VPC)
* a Subnet
* a Virtual Server Instance within the VPC and a particular region and availability zone (AZ)
* a floating IP (FIP) address on the public Internet
* a security group that allows ingress traffic on port 22 (for debug)

IMPORTANT: Reboots of the VM are not supported, and will result in loss of data. Back up any datasets or models prior to a reboot or shutdown of underlying VPC infrastructure.

NOTE: Please note that provisioning may take approximately twenty minutes.


## Standalone Terraform Deployment Steps

### Prerequisites

To run as a standalone Terraform deployment, you need the following prerequisites.

```
terraform: v0.11.x or greater
ibm terraform provider: v0.24.x or greater
```

Use the [IBM Cloud VPC Terraform Documentation](https://cloud.ibm.com/docs/terraform?topic=terraform-getting-started#install) for information on how to install Terraform and the IBM Terraform Provider.

You also need to have an [IBM Cloud API Key](https://cloud.ibm.com/docs/iam?topic=iam-userapikey).

### Installation Steps

1. Clone this git respository
2. Review the deployment attributes in the vm.tf file.  You may use the defaults.
3. Run `terraform apply`

When deployment starts, it will ask you for your API key.  The IBM Visual Insights Trial will then take ~20 minutes to launch.

### Destroy

Simply run `terraform destroy` to remove the IBM Visual Insights infrastructure.  The solution will also remove the VPC, Subnet, and all other associated resources it created.  It will not touch other infrastructure in your IBM Cloud account.


## Resources
* Engage with us on the [IBM Developer Forums](https://developer.ibm.com/answers/smart-spaces/361/powerai.html).
