#Steps to Deploy Student form using Docker Container

### Step 1: Go to Database Folder and Create A Database container
````
cd Database
````
For that first create a Database image
````
docker build -t database:d1
````
Then to run the container 
````
docker run -itd database:d1
````
To get container id 
````
docker ps
````
To get the container ip 
````
docker inspect <container id>
````
Copy the ip address of the the container

### Step 2: Go to Tomcat Folder and Create A tomcat container
````
cd ../Tomcat
````
First open the context.xml file and enter the ip address in url in resource tag 
````
vim context.xml
````
Build the Tomcat image
````
docker build -t tomcat:t1
````
To list the images
````
docker images
````
To run the container 
````
docker run -itd -p 8080:8080 tomcat:t1
````
To get the ip of container 
````
docker inspect <container id>
````
Copy the ip address of the the container

### Step 3: Go to Nginx folder and Create the Nginx Container
````
cd ../Nginx
````
First edit the nginx.conf file , add ip address of tomcat container in proxy_pass
````
vim nginx.conf
````
Build the Nginx image 
````
docker build -t nginx:n1
````
Run the Container
````
docker run -itd -p 80:80 nginx:n1
````

### Step 4: Copy the public ip and host it 

<publicip>/student
