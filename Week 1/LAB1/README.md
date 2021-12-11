# Lab 1: Create a Linux virtual machine with the Azure CLI
 Done all task for week one
1. Launch Azure Cloud Shell
2. Create a resource group
3. Create virtual machine
4. Open port 80 for web traffic
5. Connect to virtual machine
6. Install web server
7. View the web server in action

### Notes:
1
Luching an Azure Cloud shell there is an icon at the top right of the side bar, after the search bar i clicked on in then the cloud shell was lunched..

2
Creating a resource Group....in a cloud shell in Azure i used the Az at the beginning of each command..example when i wanted to create a resoure group this is the commaned i used not in full details:
  this is the command:-  "az group create --name myResourceGroup --location eastus"

3
 while creating a virtual machine i used this command 
  az vm create \
  --resource-group myResourceGroup \
  --name myVM \
  --image UbuntuLTS \
  --admin-username azureuser \
  --generate-ssh-keys
  the lines with -- or - are options 
  Options:-This modify the default behaviour of the command.
 there are short option(-) and long option(--) 

4
 port 80 is the port that the server "listens to" or expects to receive from a Web client.
 az vm open-port --port 80 --resource-group myResourceGroup --name myVM

5
 ssh into your VM using clould shell you have to use the public ip address of the VM with a command like this
 ssh azureuser@40.68.254.142

6
 Installing a web Server 
 first if you have a web server already in your system globally
 you can check the update by using this code

 sudo apt-get -y update

 while if you don't have it on your system globally you install by using this Code

 sudo apt-get -y install nginx

7
then after the installation  of your webserver you can put your public IP addresss in your brower and your




Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart