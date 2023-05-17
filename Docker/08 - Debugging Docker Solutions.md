# GO 

## QCM - Docker Compose: Debugging Docker Solutions
<br>
<br>


### **Question** : Which command can be used to obtain low-level information about containers and images including the image checksum, information about layers, and container IP address?

> `docker inspect`


#
### **Question** : Which are challenges associated with identifying the root cause of issues with microservice-based architecture?

> `Lack of observability`

> `Difficulties tracing errors`


#
### **Question** : Which command can be used for Docker Hub and for private registries to generate an authentication file?

> `docker login`


#
### **Question** : Which are valid logging driver options for Docker?

> `Fluentd`

> `Journald`

> `Syslog`


#
### **Question** : Which Docker command successfully reveals all containers on a system including containers not currently running?

> `sudo docker ps -a`

#
### **Question** : Which are delivery modes that Docker uses for writing container logs?

> `Blocking`

> `Non-blocking`


#
### **Question** : Which command successfully runs the official Docker Hub PostgreSQL database image?

> `sudo docker run --name db-postgres -e POSTGRES_PASSWORD=secret -d postgres`


#
### **Question** : Complete the Dockerfile to ensure that the image successfully installs the nano editor during the build process.

```dockerfile
# pull the base image
FROM debian:latest

# apt package list maintenance
RUN apt-get clean && <missing code>

# install nano editor
RUN apt-get install -qy nano
```

> `apt-get update`


#
### **Question** : Which Pod startup error occurs when Kubernetes cannot retrieve one of the images for the containers in a pod?

> `ImagePullBackoff`


#
### **Question** : Which is Docker's open-source script used to audit Docker containers against security benchmarks?

> `Docker bench`


#
### **Question** : Which metadata label is used to specify the email address and name of whoever is responsible for an image?

> `maintainer`


#
### **Question** : Which are traditional network troubleshooting tools that can still be effective in IaaS cloud computing services?

> `ping`

> `traceroute`

> `nslookup`

