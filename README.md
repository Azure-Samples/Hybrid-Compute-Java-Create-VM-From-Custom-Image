---
page_type: sample
languages:
- java
products:
- azure
- azure-virtual-machines
description: "Azure Compute sample for creating a virtual machine using custom vm image"
urlFragment: hybrid-compute-java-create-vm-from-custom-image
---

# Hybrid-Compute-Java-Create-VM-From-Custom-Image

Azure Compute sample for creating a virtual machine using custom vm image

- Create a virtual machine
- Delete a virtual machine


## Running this sample

To run this sample:

1. [Add a custom virtual machine image to Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-add-vm-image). Make a note of the blob storage URI where you upload the image. The blob storage URI has the following format: &lt;storageAccount&gt;/&lt;blobContainer&gt;/&lt;targetVHDName&gt;.vhd.

2. Clone the repository using the following command:

    git clone https://github.com/Azure-Samples/hybrid-compute-java-create-vm-from-custom-image.git

3. Create an Azure service principal and assign a role to access the subscription. For instructions on creating a service principal, see [Use Azure PowerShell to create a service principal with a certificate](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-create-service-principals).

4. Set the following required environment variable values:

    * AZURE_TENANT_ID

    * AZURE_CLIENT_ID

    * AZURE_CLIENT_SECRET

    * AZURE_SUBSCRIPTION_ID

    * ARM_ENDPOINT

    * AZURE_RESOURCE_LOCATION

    * AZURE_CUSTOM_IMAGE_URL (Blob storage URI value from Step 1)

5. Change directory to Hybrid sample:
    
    * cd hybrid-compute-java-create-vm-from-custom-image

6. Run the sample:
    * mvn clean compile exec:java
    
## More information

[http://azure.com/java](http://azure.com/java)

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
