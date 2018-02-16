### 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

- A docker container is designed to isolate the software it contains from the local environment so that it runs consisitently at all times, making it more compatible with other services.

- A virtual machine on the other hand, while also isolated, is self-contained and not as suited for portability like a docker container.

- Furthermore a docker container will host an application locally within the container, and can then port it over to a service, without recompiling the application, makes it very simple to deploy.

### 2. Using the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

- It specifies the mapping between the port 8080 inside the container with a port on your local machine, in this case 49160.

### 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

- It helps in keeping track of your containers. Kubernetes lets you deploy containers to clusters, keeping them organized, so that you can deploy efficiently and make sure the right container is being deployed.

### 4. How do you change the number of replicas in a Kubernetes cluster?

- When creating a cluster, there is a special syntax used where you declare the number of replicas in the num-nodes identifier. 

### 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

- Horizonatally means that you are focusing one one component at a time, moving on when it is complete and dependencies are operating as they should be. Vertically means that all components need to be deployed or running so that they can be tested more effectively.

### 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

- The free tier does not scale and will automatically shut down after a period of inactivity, usually 30 mins, which can make it difficult to deploy an app that needs to be accessed frequently. The paid tier avoids this, and is scalable making it a better choice if that is a requirement for the app.