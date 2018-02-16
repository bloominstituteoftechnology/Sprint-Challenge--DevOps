### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
  - Dockers are primarily concerned with providing containers. Containers provide a way to isolate applications and provide a virtual platform for applications to run on. Virttual machines ustilizes a software based environment to stimulate a hardware based environment. Servers can also be broken up into virualized machines that can run different operating systems. However, containers can have one single operating system on a hostwhich can run all the different apllications from the cloud. Containers essenitally allow you to virtualize the operating system itself which is why is is more portable than a virtual machine.

2. Given the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
  - First off, the docker run command runs a process in a new container. The '-p' specificies the particular process that you want to run and helps us understand the two numbers that come afterwards. This command essentially pushs a containers port to the host. The number is the sepcific port that that listening for connections. 

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm? 
- The purpose of these types of platforms is to automate deployment, scaling and operations of application containers across a cluster of hosts while providing a container esq infrastructure. It provides organization to your application across multiple machines and works as a operating system for your cluster. 

4. How do you change the number of replicas in a Kubernetes cluster?
  - One way to change the number of replicas in a Kebernetes cluster is to go into your deployment.yml file and under 'spec:' there should be a property called replicas and you can enter the number of replicas you wish to have there. 

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
  - Vertical scaling allows you to resize your server with no change to your code. It basically being able to increase the capacity of existing hard or software by adding additional resources. Horizontal scaling is the ability for a server to deal with traffic or the ability to connect with multiple hardwares or softwares so they can work as a single unit.
6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
 - The paid tiers of Heroku offer multiple advantages over the free tier including greater overall scalabiltiy handling larger traffic and with a much larger server,  handles more powerful apps using more workers, free SSL and automated certificate management, and never sleeps among many other benefits. Workers by the way is the agent responsible for running Pod containers in Docker and does status reports of Pods to the rest of the system. 