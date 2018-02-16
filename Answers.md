### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
*From a functional standpoint, Docker containers are executed with the Docker engine which do to its smaller size are innately have fast start up processes,
and therefore overall better performance than a VM.  There is a larger margin of compatability as well due to sharing of the host's kernel. Virtual machines
are essentially complete OS that operate with the same memory management and associated overhead of device drivers like their native counterparts. The resources
that are required for the VM to operate are emulated and with hypervisor, it is possible to run many instances of one or more VM's in parallel on a single machine.*

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
*this command is used to run the image in Docker. with a port mapping between port 8080 within the container and port 41960 with the local machine*

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
*if the situation were to occurr that required a devop to deploy a large number of containers, he would need a container orchestration platform in order to more easily
mange and secure those containers.  It also helps with load balancing as well.*

4. How do you change the number of replicas in a Kubernetes cluster?
*the `replicas` setting located in the `deployment.yml` file must be modified then the command `kubectl apply -f deployment.yml` must be implemented to apply those changes.*

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
*horizontally- scaling by adding more machines into a pool of resources.
vertically- scaling by adding more power by means of hardware upgrades to an existing machine.*

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
*with the free tier, users are provided a single "dyno" which is a light weight container that executes a single user-specified command.  paid tiers are allowed
to scale dynos vertically and horizontally.
