# Creating a Custom Ubuntu Apache Image from a Dockerfile  
This tutorial is a walk-through of how to create a Dockerfile and spin up an image from the Dockerfile. 
At the end of this tutorial, you will learn the bash script commands needed and how to write them in a dockerfile. 
### Pre-requisites
1. Ensure Docker service is Up and running.
   > To check if Docker service is up and running, type the `docker --status` command. If not, run the command `sudo service docker start` to start the Docker service. 
2. Use any Linux Distribution of your choice. This guide is based on Debian distribution. Linux commands might defer slightly.  
### Steps
1. Start the Docker Service
```
sudo service docker start
```
2. Create a Dockerfile with the file name **Dockerfile**
```
nano Dockerfile
```
3. Write the following script inside the Dockerfile. This script defines how to build a docker image that runs an Apache Web Server on an Ubuntu-based Container. 
```
FROM ubuntu:latest
RUN apt-get update && apt-get install -y apache2=
CMD ["apachectl", "-D", "FOREGROUND"]
```
4. Save the Dockerfile by typing **Ctrl + O** to Write Out, press Enter to accept changes. Type **Ctrl + X** to exit Nano Text Editor.
5. Now, build the Ubuntu Apache image using the following command:
```
docker build --tag ubuntu_apache:v1 .
```
6. Check to confirm if the image is built by using this command:
```
docker images
```
7. If your Ubuntu:Apache image is listed, run the image to create a Docker container
```
docker run --name ubuntu-apache -d ubuntu_apache:v1
```
8. Check to confirm if the container is running.
```
docker ps
```
9. Expose to port 9090 to view the installed Apache on the browser.

```
docker run -d -p 9090:80 --name ubuntu-apache ubuntu_apache:v2
```
You should see the following output or something similar:
```
770658432ff2286cf9f78fe1e33d76bca09a0f072493dd43eac57f6fda4252e1
```
10. Check if Apache Web Server is running, on your browser, by using the local IP or Public IP with exposed port 9090
    

