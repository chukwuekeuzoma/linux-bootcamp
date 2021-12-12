# Lab 2: Manage Linux VMs with the Azure CLI

1. Create resource group
2. Create virtual machine
3. Connect to VM
4. Understand VM images
5. Understand VM sizes
6. VM power states
7. Management tasks

### Notes:
1 
This was done in LAB1

2 
This was  done in LAB1

3
Conneting to a VM not using the cloud shell By SSH into your vm in your local terminal, after creating an instance i downloading the pem file went to my CLI changed the directory to that location where the pen file was downloaded 

My command was

chmod 400 azureuser.pem
chmod which means change mood command ... so thr terminal will be able to ready only the pem file

there was an error at first the Error was 
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0644 for '/Users/tudouya/.ssh/vm/vm_id_rsa.pub' are too open.
It is required that your private key files are NOT accessible by others.
This private key will be ignored.
bad permissions: ignore key: /Users/tudouya/.ssh/vm/vm_id_rsa.pub
Permission denied (publickey,password).

so i added sudo at the beginning of the chmod 
sudo :-super user do 

sudo chmod 400 azureuser.pem

the Error was gone and this worked for me...

secondly Am using MAC 
the other command was 

ssh -i <private key path> azureuser@20.124.210.124

private key path :- this is where you will place the path were the downloaded pem file is located

4
What i understand about VM Images this are what are used to create VM they are like bootable operating system. They are many types of images 
UbuntuServer,RHEL which is Red Hat etc.
UbuntunServer was used to create this VM tha am Currently Using..

5 
VM sizes these are memorys that are made  available to your Virtual Machine.

6
VM Power state this represents the current state of your VM 

7
Management tasks this are just like such as starting, stopping, or deleting a virtual machine or you want to create script to auotmate  repetitive or complex tasks.



Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/tutorial-manage-vm

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart