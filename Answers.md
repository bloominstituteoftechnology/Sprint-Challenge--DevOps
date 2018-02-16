### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

* Docker keeps the consistency in dev, staging and prod via snapshots/images. So we can literally run same OS, dependecies on local and remote machines via docker containers. Super easy to debug.
* Docker Containers share the OS kernel across the machine. So if a machine has n containers they can have O(1) space as they share resouces across kernels. However VMs will have O(n) space as they have different OS for each app.
* Since container occupy less space. They are easy to fire up/boot.

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

* 8080 is container post and 49160 is post of the host. So a user hitting 49160 will be redirected to 8080 which is container port.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
* These are container management platform used to scale up or scale down the number of containers based on current demand on your app.
* Can be used to define health check policy of a container. A container not passing this policy can be terminated and won't serve to customers
* Drives up utilization by automatically binning container without sacrificing availability.

4. How do you change the number of replicas in a Kubernetes cluster?
Change spec: replicas: in Deployment.yml file

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'? 

Vertical Scaling: When you add more computing power to your existing machine at the time when demand increases. Its risky, what if machines fails?
Horizontal Scaling: When you add additional resources/machines to existing infrastructure. Not risky, since it is distributed. Fast as we can distribute as per region closer to cluster of customers

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
Free tiers switch off/on with usage. For eg: if there is no traffic to server from last 30 mins. The conatiner will go to sleep and when traffic comes it will start, since starting up takes a bit of time, it will hit customer experience. However, paid tier will keep containers running all the time 

