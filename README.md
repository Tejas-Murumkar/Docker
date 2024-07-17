# $${\color{lightlightblue} \textbf{Docker 🐳}}$$

##  ${\color{lightblue} \textbf{Installation-Steps  \ (Amazon-Linux)}}$ 


````
sudo yum update -y
sudo yum install -y docker
sudo service docker start
sudo usermod -a -G docker ec2-user
newgrp docker
````
````
docker --version
````

 ## ${\color{lightblue} \textbf{Installation-Steps  \ (Docker Commands)}}$ 

1. To Pull the image form dockerhub
 ````
 docker pull <image-name>:<version>
 ````
2. To List the images
````
docker images
````
3. To Run the Container
````
docker run -itd -p <proxy_port>:<internal_port> --name <name_for_container> <images-name>:<version>
````
where,<br>
-i -> interactive<br>
-t -> terminal<br>
-d -> detach<br> 
-p -> port<br>
--name -> name for container<br> 

4. To list containers<br>

a. To List the running containers
````
docker ps
````
b. To List the total containers 
````
docker ps -a
````
5. To enter the container
````
docker exec -it <container_id>
````
6. To Stop the container
````
docker stop <container_id>
````
7. To Remove the container
````
docker rm <container_id>
````
8. To Show detail of container
````
docker inspect <container_id>
````
9. To Remove the images
````
docker rmi <image_id>
````
10. To Remove all images
````
docker rmi $(docker images)
````
11. To Stop all containers
````
docker stop $(docker ps -qa)
````
12. To Remove all containers
````
docker rm -f $(docker ps -qa)
````
13. To Remove all Stop containers
````
docker container prune 
````
