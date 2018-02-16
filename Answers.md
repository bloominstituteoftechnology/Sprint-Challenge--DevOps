### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

    A VM virtualizes hardware on which runs an entire operating system, any applications being deployed will then run in that OS. If you need to scale up with VMs you need to spin up more VMs which is resource intensive. Docker virtualizes the application layer rather than the hardware. Containers run on the Docker daemon on the host OS. Since containers don't have to carry an entire OS, they are much smaller than VM images, and they take much less time to start up, seconds or even milliseconds compared to minutes for a VM.

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

    It means bind the container's port 8080 to the host's port 49160. By doing so anything running on the container's port will be available on the host's port.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

    Container orchestration platforms automate the deployment, scaling, and operating of application containers. Production applications typically span multiple containers and multiple hosts, Kubernetes and the like make it much easier to manage everything.

4. How do you change the number of replicas in a Kubernetes cluster?

    The kubectl scale command is used to change the number of replicas in a cluster. The number of replicas can also be set in the Deployment spec.

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

    Vertical scaling is adding more resources, CPU power, RAM, etc. to an existing system. It's giving an application more power by upgrading the system it is running on.

    Horizontal scaling is running the application across multiple machines and then adding more machines to it.

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

        The free tier containers go to sleep after 30 minutes of inactivity and take some time to wake up when accessed again. The free tier also has a limited number of processes that can run.
