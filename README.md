# mongodb_Azure

Step 1: 

az group create --name myResourceGroup --location eastus


Step 2: 

az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 3 --enable-addons monitoring --generate-ssh-keys

Step 3:

az aks get-credentials --resource-group myResourceGroup --name myAKSCluster

Step 4: Create a Strorage Class (DYnamic provisioning)


