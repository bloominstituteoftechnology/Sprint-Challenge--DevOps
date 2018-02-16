1.  Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?  
_Answer:_  

  A virtual machine (VM) runs an operating system within it while containers provide a method of running an isolated application(s) on a single host operating system. A VM has its own binaries/libraries and application(s) available to it.  Containers share the host OS kernel and, usually, the binaries and libraries as well. While limiting, this makes containers exceptionally lightweight. The relatively small size and quick startup of a container makes it more aptly-suited for portability than a VM.   


2. Using the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?  
_Answer:_  

 This command serves to bind port 8080 of the container to port 49160 of the host machine.  

3.  What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?  
_Answer:_  

Container orchestration platforms are used to deploy and manage complex containerized applications. Their principal purpose is to automate and simplify deployment of new binaries, scaling, monitoring and management of containerized applications.

4.  How do you change the number of replicas in a Kubernetes cluster?  
_Answer:_  
  
  The number of replicas can be changed in deployment.yml file under "spec".  

5.  What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?_Answer:_   

_*Horizontal*_ scaling means to scale by adding more machines to the system. _*Vertical*_ scaling means to scale by adding more power (CPU, RAM) to existing machines.


6.  Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers? _Answer:_   

As of this writing (16FEB2018), Heroku offers software containers for deployment on four different tiers. In the free tier, an app's power is limited because we are only allowed one worker. In the paid tiers, we can use as many workers as necessary.  
Other differences between free and paid tiers include the fact that free containers go to sleep after 30 minutes of inactivity, do not have certificate management services for custom domains, and do not haveavailable application metrics. 





