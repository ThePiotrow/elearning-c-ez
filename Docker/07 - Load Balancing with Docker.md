# GO 

## QCM - Docker Compose: Load Balancing with Docker
<br>
<br>


### **Question** : Complete the code snippet to configure an Nginx container as a load balancer that will load balance in round-robin fashion?

```nginx
server {

    listen 80;

    resolver 127.0.0.11 valid=30s;
    set $upstream http://backend;

    location / {
        <missing code> $upstream;
    }

}
```

> `proxy_pass`


#
### **Question** : On which Docker component is the docker daemon located?

> `Docker Engine`


#
### **Question** : Which are accurate statements concerning Docker containers?

> `Containers support resource isolation out of the box`

> `Containers typically boot up in seconds`



#
### **Question** : Which command will scale a docker service named myservice to 7 replica tasks?

> `sudo docker service scale myservice=7`


#
### **Question** : To expose services externally, which type of load balancing does Swarm manager use?

> `Ingress load balancing`


#
### **Question** : Which statements accurately describe microservices?

> `They support scaling backend and frontend separately`

> `They comprise loosely-coupled services`


#
### **Question** : Which components are installed when you install Docker Engine?

> `docker-ce-cli`

> `containerd.io`

> `docker-ce`


#
### **Question** : Which command will output the swarm join command with the join token used to add workers to a swarm?

> `sudo docker swarm join-token worker`


#
### **Question** : Which are valid types of Docker networks?

> `Overlay`

> `Macvlan`

> `Bridge`


#
### **Question** : What is the name of the file that is a blueprint for Docker containers?

> `Dockerfile`


#
### **Question** : Which are challenges specific to load balancing Docker deployments?

> `Tracking load distribution`

> `Deployment complexity`


#
### **Question** : What are the reasons that advanced routing is required?

> `For terminating TLS traffic`

> `To provide complex upgrades and rollouts`


#
### **Question** : Which are benefits of fully-managed services?

> `Automated backups and failovers`

> `Hardware and software regularly updated`