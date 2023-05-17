# GO 

## QCM - Docker Compose: Advanced Docker Security
<br>
<br>


### **Question** : Which Docker run flag allows a container to run without a seccomp template?

> `--security-opt seccomp=unconfined`


#
### **Question** : Which Docker kernel namespace gives each container a unique hostname?

> `UTS`


#
### **Question** : A custom seccomp template called custom_template.json has been created for a container. Which Docker run flag will associate the container with the custom template?

> `--security-opt seccomp=custom_template.json`


#
### **Question** : Which command allows a Docker client to communicate with a remote Docker daemon?

> `docker context use`


#
### **Question** : Match the Docker model components to their descriptions.

Deamon:

> `Performs actions on containers`

Image:

> `Acts as a template for a container`

Client:

> `Communicates with daemon via REST API`

Registry:

> `Stores base images`

Container:

> `Runs on the Docker host machine`


#
### **Question** : What is the purpose of certificates for content trust in Docker?

> `Secure data to and from registries`


#
### **Question** : Which Docker run flag will run a container with only AppArmor protection?

> `--security-opt seccomp=unconfirmed`


#
### **Question** : What are some of the inherent security benefits of Docker containers?

> `Isolation`

> `Small attack surface`

> `Simple design`


#
### **Question** : Which component(s) of a Docker environment is AppArmor designed to protect?

> `Operating system`

> `Applications`


#
### **Question** : Which Docker content trust keys prevent mix and match attacks?

> `Snapshot`


#
### **Question** : Match the application deployment technologies with their benefits. Application deployment technologies may be used more than once.

Virtual machines:

> `Provides undivided access to OS resources`

> `Can run same tools as a physical server`

> `Has well understood security controls`

Docker containers:

> `Does not require a lot of management`

> `Exposes a simple interface`

> `Small and portable`