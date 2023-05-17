# GO 

## QCM - Docker Compose: Multiple Docker Containers
<br>
<br>


### **Question** : Match the docker-compose up option flag with the appropriate option description.

--force-recreate:

> `Recreates all containers even if they did not change`

> `Incompatible with the --no-recreate option`

--no-recreate:

> `Does not recreate any containers even if they have changed`

--always-recreate-deps:

> `Recreates dependency containers`

> `Incompatible with the --no-recreate option`


#
### **Question** : What feature does Docker Compose provide to enable container customization for various environments and users?

> `Variables`


#
### **Question** : What command is the correct way to invoke docker-compose up with multiple Compose files?

> `sudo docker-compose -f docker-compose.yml -f docker-compose.prod.yml up -d`


#
### **Question** : Sequence the steps in order to set up a multi container Docker application using a MYSQL database container.

> `Create a new network`

> `Start the MYSQL container passing in the --network and --network-alias flags`

> `Try connecting to the database container to confirm that it is up and running`

> `Start the application container on the same network as the database container passing in values for the MYSQL environment variables`


#
### **Question** : Sequence the steps in order for a typical developer workflow when developing, testing, and deploying Docker containerized applications.

> `Develop and test the container code in a local developer environment`

> `Push the container code to a Git repository for review by the team`

> `Run the container in a test environment and execute manual and automated test cases`

> `Fix any bugs in the container code and commit, push, and retest in the test environment`

> `Deploy the container into a production environment`


#
### **Question** : Which are storage categories for Docker containers?

> `Graph`

> `Volume`

> `Registry`


#
### **Question** : Which statements regarding the docker-compose.yml file are true?

> `The docker-compose.yml file defines all the services and dependencies required to run a multi-container application in an isolated environment`

> `The docker-compose.yml file is located in the root directory of a project`


#
### **Question** : Sequence the steps in order to add new containers to a Python Flask project.

> `Look up the container to add in Docker Hub`

> `Get the correct container version tag and add it to the docker-compose.yml file`

> `Add the dependency to the requirements.txt file`

> `Make code changes to the core project files`

> `Save the project and run docker-compose up to run the application`


#
### **Question** : What key is available in the docker-compose.yml file to allow the modification of code on the fly?

> `Volumes`


#
### **Question** : Sequence the steps in order to debug a Python Flask project in Docker Compose using Visual Studio Code.

> `Add a breakpoint in the application code`

> `Add a new debug configuration and set it as the active configuration`

> `Generate the docker-compose.debug.yml file`

> `Right click the docker-compose.debug.yml file and select Compose Up`

> `Press the F5 key to attach the debugger`


#
### **Question** : What is the purpose of the .env file in a Docker Compose project?

> `Sets the default environment variable values for the Docker Compose .yml configuration file`


#
### **Question** : What are differences between Docker images and Docker containers?

> `Docker images are built through a Dockerfile`

> `Docker containers are runnable instance of images`

