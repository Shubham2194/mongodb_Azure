# mongodb_Azure


![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/ebda7ff5-4fac-4026-8bf9-5f6834326467)


Step 1: 

az group create --name myResourceGroup --location eastus


Step 2: 

az aks create --resource-group myResourceGroup --name myAKSCluster --node-count 3 --enable-addons monitoring --generate-ssh-keys

Step 3:

az aks get-credentials --resource-group myResourceGroup --name myAKSCluster

Step 4: Create a Strorage Class (DYnamic provisioning)

![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/27c68386-8dca-40b9-9a35-5bcad221c690)


kubectl apply -f storage-class.yaml

Step 5: Create Secrets

![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/6f8dbc36-ea4f-4c2f-ad9b-a36d4c7bbc44)


kubectl apply -f secret.yaml


Step 6: Deploy MongoDB with StatefulSet

![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/10ddfa48-535c-4452-84db-78f3e1c80796)


kubectl apply -f mongodb-deploy.yaml

Step 7: Expose mongoDB

![image](https://github.com/Shubham2194/mongodb_Azure/assets/83746560/9bf5f3d2-60d1-4503-b848-6967264a81b9)

kubectl apply -f svc.yaml

kubectl get all



Mongodb with one replica deployed having persistent volume of 20Gi on AKS :)

