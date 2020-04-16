# Terraform v0.12

This folder contains the terraform files that support Terraform 0.12. 

## Dependencies

These templates were tested using Terraform 0.12.24 and the IBM Provide plugin version 1.4.0

## terraform.tfvars

You must provide the the following variables in terraform.tfvars file in order to execute these templates. Your IBM Cloud account must have the priveleges to create Gen 2 VPCs and virtual machines within those VPCs

* ibmcloud_api_key = "your IBM API key"
* icos_endpoint = "the endpoint of an existing IBM Cloud Object Storage bucket"
* icos_key = "the access key to the ICOS bucket"
* icos_secret = "the access key secret to the ICOS bucket"


## <span>variables.tf</span>

The <span>variables.tf</span> file contains values for the following variables. Change them if you wish.

* vpc_basename - the base name of the VPC that is created
* boot_image_name - the specific Ubuntu image used for the VM
* vpc_region - the IBM Cloud region the VPC will be created in
* vpc_zone - the availability zone within the region
* vm_profile - the specific VM machine architecture
* icos_bucket - the name of the predefined ICOS bucket
