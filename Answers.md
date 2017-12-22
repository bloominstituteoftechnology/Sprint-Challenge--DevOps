### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

* 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
Answer: A virtual machine runs a operating system in it. A VM has its own binaries/libraries and application(s) that it runs.
On the other hand, containers provide a way to run isolated applications on a single host operating system. Each container shares the host OS kernel and, usually, the binaries and libraries, too. This makes containers exceptionally lightweight. Containers are only megabytes in size and take just seconds to start, versus minutes for a VM.

* 2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
Answer: This command binds port 8080 of the container to port 49160 of the host machine.

* 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
Answer: Container orchestration platform automate and simplify deployment of new binaries, scaling, monitoring and management of containerized applications.

* 4. How do you change the number of replicas in a Kubernetes cluster?
Answer: The number of replicas can be changed in deployment.yml file under "spec".

* 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
Answer: Horizontal scaling means to scale by adding more machines to the system. Vertical scaling means to scale by adding more power (CPU, RAM) to existing machines.

* 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
Answer: In the free tier, we only get 1 worker/machine to use. While in the paid tier, we can use as many workers/machines as we need.