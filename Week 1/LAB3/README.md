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

 4
  This has already been done in the recent Labs 

 5
  Create and attach disks
   
   When A virtual Machine is created or you already have an existing virtual machine Data disk can be created and attached.

   This is the command i used when creating a VM so i added a command line where the data disk is also created.

   "az vm create --resource-group myResourceGroupDisk --name myVM --image UbuntuLTS --size Standard_DS2_v2          --admin-username azureuser   --generate-ssh-keys  --data-disk-sizes-gb 128 128"

  while this command below is used to attach the Data disk into a VM 

    "az vm disk attach  --resource-group myResourceGroupDisk --vm-name myVM --name myDataDisk --size-gb 128 --sku Premium_LRS --new"

 6 Prepare data disks
    Still Working on it.

 7 Take a disk snapshot
   Snapshots in VM  are useful to quickly save the state of your VM before you make configuration changes.In the event of an issue or error, VM can be restored using a snapshot. When a VM has more than one disk, a snapshot is taken of each disk independently of the others. To take application consistent backups, consider stopping the VM before you take disk snapshots

   Before you create A Snap Shot  You need the ID or the name of the Disk
   by using this command.

   "osdiskid=$(az vm show  -g myResourceGroupDisk -n myVM --query "storageProfile.osDisk.managedDisk.id" -o tsv)"

   now that you have the ID you can create a snapshot

   "az snapshot create --resource-group myResourceGroupDisk --source "$osdiskid" --name osDisk-backup"


Quickstart: Manage Azure disks
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-disks

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart