1.	Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

As I understand it, Docker containers are less bulky and require less of a user’s machine instead of a VM which, because they are emulating an environment, require huge amounts of memory. Sometimes a VM is necessary when you need a highly controlled environment. A container is lighter weight because of the use of the Linox kernel which allows for the sharing of resources.

2. 	Given the commend docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

The 8080 references the port within the container and the 49160 specifies the port on the user’s machine.

3. 	What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

They allow you to automate the deployment of multiple containers as an application is developed. It helps build relationships between the different containers, allows for scaling in or out and helps in upgrade transitions.

4. How do you change the number of replicas in a Kubernetes cluster?
```
$ kubectl scale rc NAME --replicas=COUNT \
    [--current-replicas=COUNT] \
    [--resource-version=VERSION]
```
5.	What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Vertically scaling means adding more processing power or memory, it adds more juice to the same code. Horizontally scaling means having multiple servers to handle multiple requests, in order to accomplish this, your application must be decoupled, be written to have several smaller servers rather than one giant server.

6.	Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

The free tier will put your application to sleep after 30 minutes whereas the paid versions allow your application to be accessible solongas you don't go over your memory limitations.