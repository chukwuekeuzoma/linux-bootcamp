# Lab 3: Manage Azure disks with the Azure CLI

1. Default Azure disks
2. Azure data disks
3. VM disk types
4. Launch Azure Cloud Shell
5. Create and attach disks
6. Prepare data disks
7. Take a disk snapshot

### Notes:

1
Default Azure Disks
 They are two disk which are automatically attached to the virtual Machine 
 we have the operating system disk & Temporary Disk

 The operating System Disk cn be size up to 2TB, because of its configuration the OS(Operating system )shoild not be used for Applications and Data.

 While the Temporary Disk this are highly performance and acn be used as a temporary data processing. whereby if the VM is moved to a new host the data stored in the  temporary disk is removed. 

 2
 Azure Data Disks 
 For the installation of applications and data storage additional disk is added.
 The size of your virtual machine determines how many datas that can be added or attached to your VM.

 3 VM disk type 
 Azure provide for us two types of disks which are the Standard disks and the Premium disks
 the difference between the both of them is that the Standard disks is backed by HDDs while the Premium disks is backed by SSD. Premium disks are preferable because of its high performance  low latency disk and its perfect for VMs running production workload.

 while the Standard Disks this delivers high cost when been in performance.



Quickstart: Manage Azure disks
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-disks

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart