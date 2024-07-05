# mongodb_Azure

Step 1: 

az group create --name myResourceGroup --location eastus


Step 2: 

az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 3 --enable-addons monitoring --generate-ssh-keys

Step 3:

az aks get-credentials --resource-group myResourceGroup --name myAKSCluster

Step 4: Create a Strorage Class (DYnamic provisioning)

![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/c6394b1f-5244-40c5-ab4b-448d3d31e269)

kubectl apply -f storage-class.yaml

Step 5: Create PVC

![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/e0aea836-9e5c-4919-919f-6818858405fe)

kubectl apply -f mongo-pvc.yaml

Step 6: Deploy MongoDB with StatefulSet

kubectl apply -f mongo-statefulset.yaml

Step 7: 

kubectl get all

Mongodb with one replica deployed on AKS :)

