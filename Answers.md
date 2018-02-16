### Your responses to the short answer questions should be laid out here using markdown.

1. Describe the differences between a Docker container and a virtual machine (VM). What makes a container more aptly-suited for portability?

While both, Docker container and VM, sit on top of a host operating system and provide a way to isolate applications they do so in different ways with each having pros an cons. A VM has its own complete operating system, where as Docker uses the kernel of the host operating system. Because of this a VM has a much larger size and in slower is speed because the host machine is running two operating systems. With is size it is much harder to run another VM inside of a VM. However because a VM uses its own operating system, a it can be hosted by a different operating system. Also because there is less interface with the host system, there is lesser security risk to both the VM and the host operating system
  
On the other hand, Docker is more portable because of it smaller size. Decker container work well inside of other Docker containers. They are very fast to start and create. With out the hugh space cost of additional operating systems, a host machinc can hold more Docker containers than it can hold VMs. However with Docker, because it uses the host kernel the applications running on it must working with the host system and the is a higher security risk to both.
  
2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

`49160:8080` specifies that Docker is using proxy port 49160 to run the application that is normally run on port 8080

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
4. How do you change the number of replicas in a Kubernetes cluster?
5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
