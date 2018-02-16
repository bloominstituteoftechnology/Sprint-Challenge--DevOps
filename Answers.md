### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Assessment Questions
#### RESEARCH AND THOROUGHLY Answer these questions. This shouldn't take just a trivial amount of time. You should spend some signifigant time on this.
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

A Docker container and a virtual machine both provide an isolated environment to run an application. In addition, the environment can be moved beetween hosts. 
A virtual machine is self-contained and possess its own infrastructure.
The docker container shares infrastructure with all other docker containers. A container isolates software from its environment so it always runs the same. This can reduce conflicts introduced with running the application over different softwares.
A docker container is well suited for portability because you can host an application inside a container and then port it over to a different operating system without having to recompile anything.
This means that you can have one docker container and use it in many places, which is extremely convenient.

2. Using the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

8080 is the port you are describing in your code. It is the local port from your device that you would like to expose the code through. 49160 is the forwarding address port that docker is going to use in order to publish your code visibly.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

These are two options for deployment in such a way that they are replicated over multiple nodes. I believe this is to handle larger loads of users and to make sure the service stays online even if a node goes down.


4. How do you change the number of replicas in a Kubernetes cluster?

You specify the number of nodes when creating a cluster with num-nodes, which makes up a swarm. You can change node availability by running docker node update on the command line. Kubernetes seems to be the more fleshed out choice, and is supported by Google.

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Vertical deployment requires all tiers and components to be deployed in order to test any of them. This has a greater comparative complexity. 
Horizontal deployment focuses on one component or one tier at a t time. It assumes that any dependencies are working and provided. This speeds up integration and has lower complexity. This is said to increase a developer's productivity, since you can focus on smaller components rather than having to know the ins and outs of the entire application in full.


6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

Something that I noticed when examining the different tiers of Heroku is that on the free tier the support will go to sleep after a period of 30 minutes of inactivity. The paid tier does not. Online there were a number of people who complained because when it goes to sleep it needs to be pinged to come out of that, so if a customer goes to the site and doesn't refresh it a time or two they might think the system is down and that is going to lead to a bad customer experience. 
Horizontal scalability is also introduced at a paid tier, as are application metrics for monitoring your application.