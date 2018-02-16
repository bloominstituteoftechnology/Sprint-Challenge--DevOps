### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

A docker container is an image of a project and its dependencies. With docker, the software image can run on any operating system and take up less resources during run time.

A virtual machine mimics the behavior of an operating system. Software running on a VM must physically include it's dependencies causing bloat and slower runtimes when compared to docker.

### Given the commend docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

The left side of the colon specifies the location of the host. For windows this is an IP address, for Mac its localhost. The right side of the colon is the port where the software is running

### What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

A container orchestration platform can host a series of software containers in the cloud and run them based on the needs of each container

### How do you change the number of replicas in a Kubernetes cluster?

You can delete them

### What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Scaling horizontally means adding more machines to support your infrastructure. Scaling vertically means adding more power to the machines that run your software.

### Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

The free tier of heroku will sleep your software when it is not in use. This means a reboot for the first user returning to your software while its sleeping. This can take as long as 10 seconds translating to a poor loading experience for that user. 

With paid tiers you can specify the needs of your software including fully dedicating hosting

