# Sprint Challenge | DevOps

----
### Q1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability??

> A1. Docker containers and virtual machines are the two main ways to deploy services on a single platform. ***WIP***

### Q2. Using the command ```docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>```, what does ```49160:8080``` specify?

> A2. When running the image, you can run the image in detached mode using ```-d```, or run it by redirecting a public port to a private port inside the container by using the ```-p``` flag. 

> In either method, when writing ```49160:8080```, docker is mapping the 8080 port inside of the container to the port 49160 on your machine.

### Q3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

> A3. These are clustering and scheduling tools for Docker containers. With these, admins and devs can establish and manage a cluster of Docker nodes as a single virtual system.

### Q4. How do you change the number of replicas in a Kubernetes cluster?

> A4. The kubectl command changes the number of replicas in a cluster, but the number of replicas can also be set in the Deployment spec.

### Q5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

> A5. Vertical scaling is adding more resources to an individual machine to handle a load, while horizontal scaling involves adding more machines to spread the load.

### Q6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

> A6. The free one takes naps after 30 minutes and waking it up can be costly in the time it takes to ping awake. 

> Free tier offers no horizontal scaling, no application metrics, and no monitoring of the application.
