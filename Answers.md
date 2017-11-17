# Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

A Docker container is an image that contains everything needed to run some software whereas a virtual machine is an entire os running on another os. Both Docker and virtual machines isolate themselves from the OS they are running on, but docker itself is just software being executed by the OS.

# Given the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

You are binding port 49160 of the host machine to the docker machine port 8080. So you are essentially forwarding traffic from port 49160 to the docker machine port 8080

# What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

Container orchestration platforms allow you to manage clusters of docker images to scale your software to meet demands.

# How do you change the number of replicas in a Kubernetes cluster?

`kubectl scale deployments/<name> --replicas=2`

# What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Horizontal scaling is done by adding more hardware to the cluster such as adding more ram or a whole other server.

Vertical scaling is done by adding more resources to the containers but is limited to the amount of resources available on the server.

# Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

In the free version you are limited to a single worker, .5gb ram, it sleeps after 30 min of inactivity, and you are limited to 1000 hours a month of use or 550 hours of use for an unverified account. 

The lowest paid teir gives you 10 process types, it never sleeps, you can use it as much as you want per month.

The higher tiers offer up to 14gb of ram, unlimited process types, horizontal scaling, autoscaling, and zero downtime.
