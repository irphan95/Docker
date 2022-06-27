# Docker
## *Installation of Docker in ubuntu* 
- #### Type sudo snap install docker or sudo apt  install docker.io to initialize the process of installation of docker
![image](https://user-images.githubusercontent.com/103019032/162897026-57266f2d-737e-474e-b9ec-301631786af0.png)
- #### After installation of docker we will check the docker version
- #### sudo docker version
![image](https://user-images.githubusercontent.com/103019032/162898133-43a8a34d-1aa0-4815-b95f-acc377eb0f83.png)
- #### Go to the docker hub website and sigin,if you already have account then go to the signin 
![image](https://user-images.githubusercontent.com/103019032/162900681-bf9668cd-342c-4330-b56e-a71cd3069b22.png)
## *Docker images*
- #### To download a Docker image called CentOS 7, issue the following command.
- #### sudo docker search < image name >
![image](https://user-images.githubusercontent.com/103019032/162905287-900e335e-6013-4a8a-9768-38bb8a54bbaa.png)
- #### Download it locally by running the below command (in this case a CentOS image is downloaded and used).
- #### sudo docker pull < image name >
![image](https://user-images.githubusercontent.com/103019032/162906151-41f9c72a-d168-4ac5-8918-e3ed6109d863.png)
- #### To list all the available Docker images on your host run the following command.
- #### sudo docker images
![image](https://user-images.githubusercontent.com/103019032/162906436-4cea1306-450b-4926-a1b7-7d8c6e572877.png)
- #### If you don’t want a Docker image anymore and you can remove it using the following command.
- #### sudo docker rmi < image name >
![image](https://user-images.githubusercontent.com/103019032/162906851-5df2fd3c-3b04-407b-ab3f-4087c4dc4b3e.png)
## *Docker container*
- #### To run the containers again, first you need to get the Container ID or Name by running the following command
![image](https://user-images.githubusercontent.com/103019032/162923344-9c50f4f4-cd63-49af-b702-3a950fa2e414.png)
- #### Once the Container ID or Name has been acquired, you can start the container using the following command
- #### sudo docker start < container id >
![image](https://user-images.githubusercontent.com/103019032/162924431-f16418c4-41c9-4527-acf3-b3a2c578700d.png)
- #### To stop the running container run docker stop command by specifying the Container ID or Name
- #### sudo docker stop < container id >
![image](https://user-images.githubusercontent.com/103019032/162925471-716fcc8c-fac1-4a7a-b377-883c74e869ea.png)
## *Dockerfile*
- #### create a file using vi editor and cat command is used to display the content
![image](https://user-images.githubusercontent.com/103019032/162944315-f97ac60d-8502-42f8-bdd3-ad4ccfb2d978.png)
- #### The docker build command file execute stepwise
![image](https://user-images.githubusercontent.com/103019032/162945182-2dd55b07-ddd5-4366-8a15-5b3a722f5b84.png)
 ## *Managing ports in Docker*
 - #### logged into docker hub
 ![image](https://user-images.githubusercontent.com/103019032/162949345-35c334c0-5300-402b-8465-f2c2509a2e1a.png)
- #### Next, let’s browse and search the Jenkins image
![image](https://user-images.githubusercontent.com/103019032/162949916-c3334863-856d-44f9-9034-d9420b979645.png)
- #### you can see the Docker pull command. This will be used to download the Jenkins Image onto the local Ubuntu server
![image](https://user-images.githubusercontent.com/103019032/162951312-934965d9-19de-4c78-a92c-664d6e919b79.png)
- #### Now go to the Ubuntu server and run the command
![image](https://user-images.githubusercontent.com/103019032/162951647-8f0fe9c9-1ca5-4435-8236-8d5601b81aa2.png)
- #### To understand what ports are exposed by the container, you should use the Docker inspect command to inspect the image
![image](https://user-images.githubusercontent.com/103019032/162952088-500b10b0-6747-4166-a4af-d28933218c93.png)
- #### To run Jenkins and map the ports, you need to change the Docker run command and add the ‘p’ option which specifies the port mapping. So, you need to run the following command
![image](https://user-images.githubusercontent.com/103019032/162956898-b6abee4d-644a-4adc-8ede-56a8a0b34bca.png)
## *Docker networing*
- #### The command will output all the networks on the Docker Host
![image](https://user-images.githubusercontent.com/103019032/162958677-06354691-ffa5-4b5a-bac2-21ffc6c0005f.png)
- #### sudo docker network inspect bridge command will output all the details about the network
![image](https://user-images.githubusercontent.com/103019032/162959221-4e1f167b-d7a0-4b85-89a8-86a0cc11f37b.png)Creating Your Own New Network
- #### Creating Your Own New Network
![image](https://user-images.githubusercontent.com/103019032/162960182-0180aa97-f836-438e-8d94-bfb06d0aec8a.png)
- #### This command will be used about network information
![image](https://user-images.githubusercontent.com/103019032/162960531-f4e71e1f-d47e-47de-89f8-f524b0434b59.png)
## *Docker private repo*
- #### Use the Docker run command to download the private registry. This can be done using the following command
![image](https://user-images.githubusercontent.com/103019032/163169614-2eb4b082-1844-4714-81d4-da2237e61928.png)
- #### Let’s do a docker ps to see that the registry container is indeed running
![image](https://user-images.githubusercontent.com/103019032/163170120-4bcdb9c5-2e05-4a89-89a0-78113dd31ea9.png)
- #### In our example, since we have the centos image available locally, we are going to tag it to our private repository and add a tag name of centos
![image](https://user-images.githubusercontent.com/103019032/163171113-1b3411e7-a1cd-469a-9a6b-617c196b699c.png)
- #### Now let’s use the Docker push command to push the repository to our private repository
![image](https://user-images.githubusercontent.com/103019032/163171533-5832d284-74c5-4fba-b62b-403d792a64b8.png)
- #### Now let’s delete the local images we have for centos using the docker rmi commands. We can then download the required centos image from our private repository
![image](https://user-images.githubusercontent.com/103019032/163171973-1fa6b911-ad19-4b03-80b0-7fce6b596e7c.png)
- #### Now that we don’t have any centos images on our local machine, we can now use the following Docker pull command to pull the centos image from private repository
- ![image](https://user-images.githubusercontent.com/103019032/163173242-e7aa869f-3e41-4843-adfb-ea91e0e03e7b.png)
## *DOCKER compose*
- #### Run the following command to download the current stable release of Docker Compose:
![image](https://user-images.githubusercontent.com/103019032/163758278-2b3a6c6b-2ede-4007-907f-dba461d6ff10.png)
![image](https://user-images.githubusercontent.com/103019032/163758366-c5ae1e8c-bbb5-4275-b9fe-62b2013e1974.png)
- #### Apply executable permissions to the binary
![image](https://user-images.githubusercontent.com/103019032/163758471-d278c5e9-5cbc-49b9-87c1-4eca0b2b9239.png)
- #### Test your installation type $docker compose version
![image](https://user-images.githubusercontent.com/103019032/163758608-eff20d20-cc77-4750-8772-176053e8c13e.png)
## *How to create docker compose file*
- #### To create a docker compose file make first .yml extension
![image](https://user-images.githubusercontent.com/103019032/163762541-5ee68e4d-e5c9-4a9f-a249-c6060c332a19.png)
- #### edit file using vim editor
![image](https://user-images.githubusercontent.com/103019032/163769858-c8d85131-0dea-47c6-95e4-2b043bb1d51d.png)
- #### Create docker compose
![image](https://user-images.githubusercontent.com/103019032/163770148-fd6e7a7f-9b43-4f68-9b3d-eb8610f33ce3.png)
- #### Adding multiple services in docker compose file
![image](https://user-images.githubusercontent.com/103019032/163771489-8c0df3cc-915f-4fa4-8a76-eb946dee607c.png)
- #### If we create docker compose it will start from new service
![image](https://user-images.githubusercontent.com/103019032/163771743-3238fdd3-9f0b-4420-b12a-fa6c33abc185.png)
- #### Stop docker compose using $docker compose down command
![image](https://user-images.githubusercontent.com/103019032/163772606-f0bd7679-c2bd-410c-9c28-ff7d6be24969.png)





