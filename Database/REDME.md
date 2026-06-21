# Step 1:

follow instrections of 

install-helm-CBS-csi-drive(1)

file 


# step 2: 
vim secret.yml

kubectl apply -f secrets.yml

# step 2:

vim ebs-sc-pvc.yml

kubectl apply -f ebs-sc-pvc.yml


# step 3: 

vim ClusterIPServices.yml

kubectl apply -f ClusterIPServices.yml

# step 4

vim statfullset.yml

kubectl apply -f  statfullset.yml



#
kubectl exec -it mariadb-0 -- mariadb -u root -p


