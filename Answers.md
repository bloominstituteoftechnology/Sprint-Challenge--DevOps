### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Describe the differences between a `Docker container` and a `virtual machine`. What makes a container more aptly-suited for portability?

VMs and Containers differ on quite a few dimensions, but primarily because containers provide a way to virtualize an OS in order for multiple workloads to run on a single OS instance, whereas with VMs, the hardware is being virtualized to run multiple OS instances. Containers’ speed, agility and portability make them yet another tool to help streamline software development.

2. Using the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

It's means you can use deploy the image on docker url 49160 rather the local host 8080

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

It allows you package up your app and run it on other servers.

4. How do you change the number of replicas in a Kubernetes cluster?

You can specify how many pods should run concurrently by setting .spec.replicas. The number running at any time may be higher or lower, such as if the replicas were just increased or decreased, or if a pod is gracefully shut down, and a replacement starts early.

If you do not specify .spec.replicas, then it defaults to 1.

5.  What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Vertical scaling can essentially resize your server with no change to your code. It is the ability to increase the capacity of existing hardware or software by adding resources. Vertical scaling is limited by the fact that you can only get as big as the size of the server.

Horizontal scaling affords the ability to scale wider to deal with traffic. It is the ability to connect multiple hardware or software entities, such as servers, so that they work as a single logical unit. This kind of scale cannot be implemented at a moment’s notice.

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

The difference is that the free 'tier' goes to sleep after a period of time and your application will be down.





