### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

A docker container sits on top of a physical server and operating system and usually shares the same kernel, binaries, and libraries while a virtual machine runs an operating system in a isolated environment. Containers are lighter and faster than virtual machines so they are better for portability. 


2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

*It specifies the mapping between the 8080 port inside the docker container and my local port of 49160. 


3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

*When an application gets larger, it is necessary to split it into smaller pieces. A container orchestratin platform helps in streamlining the process of automating deployments, scaling, etc. 


4. How do you change the number of replicas in a Kubernetes cluster?

*You can change it by modifying the replicas field in the deployment.yml file. 


5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

*Horizontal scaling means growing larger by connecting multiple servers to act as a single unit while vertically means to increase the size of a single server. 


6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

*The main difference is that the free tier containers go to sleep for a period of time if not in use and the paid tiers do not. 