## Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
A container is a standalone package/image that includes program code as well as the correct tools/libraries to make that code work. A virtual machine includes all of this, but also another layer -- the operating system running the virtual machine. Docker containers share an operating system and can also build on common libraries to make things more efficient.

## Given the commend docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?
49160 is the container port and 8080 is the host port. So when you access port 8080, it will be bound to whatever 49160 points to within the Docker container.

## What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
Facilitating scalability (often at an enterprise level) by managing and integrating containers to function as one entity. Allows for greater automation and provides a more robust infrastructure.

## How do you change the number of replicas in a Kubernetes cluster?
By changing the number specified in the .yml file.

## What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
Both refer to adding more hardware in order to support scaling. Horizonal scaling means increasing the number of machines; vertical scaling means increasing the power of existing machines.

## Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
The free tier limits the number of hours you can use the service per month and automatically sleeps after a period of inactivity. You're also limited in the number of applications and workers you can have.