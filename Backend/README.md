# PROCESS 1 st

# STEP : 1
ssh the another instence 

# docker installation

https://docs.docker.com/engine/install/ubuntu/

# clone project 
git clone https://github.com/Digvijay-khairnar/CDEC-studentapp.git

cd CDEC-studentapp/backend

# and updat the project with new configuration update the cluster ip in 

vim backend/src/main/resources/application.properties

   server.port=8080
   spring.datasource.url=jdbc:mariadb://<Cluster_IP>:3306/<DB_NAME>
   spring.datasource.username=<DB_USER>
   spring.datasource.password=<DB_PASS>


# STEP 2 

create the docker file for backend

vim /backdend/Dockerfile

docker build -t backend .

docker login -u 

docker tag digvijaykhairnar/backend:latest

docker push digvijaykhairnar/backend:latest

# my-eks

vim NodePort.yml

kubectl apply -f NodePort.yml

vim deploymentset.yml

kubectl apply -f deploymentset.yml

