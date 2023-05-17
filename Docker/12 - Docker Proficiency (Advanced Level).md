# GO 

## QCM - Docker Compose: Advanced Docker Orchestration
<br>
<br>


### **Question** : The Docker Engine is comprised of what three components?

> `Server, API, Command Line Interface.`


#
### **Question** : Which could be considered benefits of Docker containers?

> `Increased efficiency`

> `Rapid deployment`


#
### **Question** : In the scatter/gather design, an external client sends a request to the which node?

> `Root`


#
### **Question** : What is the name of the file that is used to configure the app services?

> `docker-compose.yml`


#
### **Question** : Where is the best place to store your Docker compose file?

> `In the application folder`


#
### **Question** : What does CI/CD stand for?

> `Continuous Integration/Continuous Delivery`


#
### **Question** : Once a docker image has been built, where can it be stored?

> `Docker registry`


### **Question** : The Docker REST API endpoint uses what kind of socket instead of a TCP one?

> `UNIX`


#
### **Question** : Which command can you use to test your Docker image locally?

> `docker run`


#
### **Question** : The Docker daemon can be configured by modifying which configuration file?

> `daemon.json`


#
### **Question** : Which are challenges associated with identifying the root cause of issues with microservice-based architecture?

> `Lack of observability`

> `Difficulties tracing errors`


#
### **Question** : Which metadata label is used to specify the email address and name of whoever is responsible for an image?

> `maintainer`


#
### **Question** : Which are delivery modes that Docker uses for writing container logs?

> `Blocking`

> `Non-blocking`


#
### **Question** : Which is Docker's open-source script used to audit Docker containers against security benchmarks?

> `Docker bench`


#
### **Question** : Which command can be used for Docker Hub and for private registries to generate an authentication file?

> `docker login`


#
### **Question** : Which aspects of Docker containers can slow down builds?

> `Image size`


#
### **Question** : The following Docker command is run:

```bash
docker run -it --memory="1g" --memory-swap="2g" mysql
```

### How much swappable memory will be available to the resulting container?

> `1 GB`


#
### **Question** : Two Docker containers running on the same host are using different operating systems from one another internal to their containers. When they run together, they use up all the disk storage on the host.
### Which Docker performance issue is occurring?

> `Resource constrained host`


#
### **Question** : What are the bottleneck(s) that can affect Docker container performance?

> `CPU usage`

> `Disk usage`

> `Memory usage`


#
### **Question** : Which Docker performance consideration can reduce the number of layers of an image?

> `Using chain commands`


#
### **Question** : What are the task(s) performed by container orchestration?

> `Scaling containers`

> `Networking between containers`

> `Managing hosts`


#
### **Question** : What are the benefit(s) of Docker orchestration tools?

> `Quality`

> `Security`

> `Simple deployments`

> `Portability`


#
### **Question** : Which cloud-based orchestration service(s) are designed to manage single stand-alone containers?

> `Azure Container Instances`

> `Google Cloud Run`


#
### **Question** : An organization writes software that processes oil well production. They create a container service that handles production data ingress. To handle increased ingress, the service scales out to multiple containers. Well sites send their ingress data to a common URL, where it is load balanced across the multiple containers.
### Which aspect(s) of orchestration and cluster management does the scaling of containers represent?

> `Orchestration`

> `Clustering`


#
### **Question** : Which Docker swarm node availability status indicates that tasks previously running on the node have been shut down?

> `Drain`


#
### **Question** : What are some of the inherent security benefits of Docker containers?

> `Isolation`

> `Small attack surface`

> `Simple design`


#
### **Question** : What is the purpose of certificates for content trust in Docker?

> `Secure data to and from registries`


#
### **Question** : Which Docker content trust keys prevent mix and match attacks?

> `Snapshot`


#
### **Question** : Which command allows a Docker client to communicate with a remote Docker daemon?

> `docker context use`


### **Question** : Which Docker run flag allows a container to run without a seccomp template?

> `--security-opt seccomp=unconfined`