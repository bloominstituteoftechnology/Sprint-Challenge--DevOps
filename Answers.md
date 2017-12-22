### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

Both Docker containers and virtual machines provide similar functionality, while the Docker containers are better for portability, virtual machines can be better for heavy computing.

Docker containers utilize the resources of a machine to run an application. All the necessary pieces to boot the desired application are housed and isolated within the container. Containers simply borrow the resources that are readily available and can share those resources without conflicts, do to their isolation.

A virtual machine by contrasts emulates a system hardware to run a complete operating system(OS). This essentially turns 1 server into many via virtualization. Each machine however runs it's own OS, and all the necessary files to boot that OS. This makes the virtual machine a much heavy option for running a few applications. 

To sum it up the biggest difference is that Docker containers utilize and share available resources and are restricted/governed by the containers isolating features so no container/application can strip away all the system resources that would be needed to run in unison with other applications. Containers are lightweight and much quicker to load than virtual machines, mainly because they have a fraction of the overhead.

Virtual machines can be slow to boot and much-less efficient than containers, virtual machines are required to boot and load ALL the files necessary to run a full OS. In comparison, Docker containers are 10's of MB's in size, while virtual machines can exceed 10's of GB's in size.


2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
This command opens up port 49160 on the local machine and broadcasts that data onto the internet via port 8080, as that's a universal port; most computers can pick up that port and are configured to listen for port 8080, once picked up the data can be transferred to a more obscure port to free up port 8080 for additinal contacts.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

Since each container is an isolated piece of software; it allows for a unique troubleshooting, deployment, and update environment. Changes can be made on each individual container or applications without affecting the surround applications. The benefits of this isolation is also it's biggest con, since the applications are so isolated they cannot work together or communicate without additional help. Where a virtual machine runs ALL the necessary pieces for an application, (OS and everything required to run an OS), containers share resources readily available, and their isolation can be used to prevent a particularly heavy service from dominating the available resources; 
To combat this isolation the need for container orchestration platforms arose, these are used to link containers together to allow them to work in unison toward a common goal; without conflicting with the benefits of isolated containers.
the term container orchestration platform alludes to many containers working/playing together to create a fully functional application/symphony.

4. How do you change the number of replicas in a Kubernetes cluster?
You can change the number of replicas in a Kubernetes cluster by scaling it up or down. You first run a command to watch the Pods in a StatefulSet and then adjust the scale to change the replicas. Afterwards you run the watch command to verify that you modification was successful.

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Scaling horizontally is creating and destroying app instances to support more users.
Scaling vertically is increasing the computing power allocated to the applications; allowing for more memory and disk space to be used, to help facilitate smoother operation.


6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

The biggest difference between the free and paid tiers are the amount of hours allocated for the use of the applications. While free applications only have a set amount of hours they can be active, the paid tier removes this restriction.

