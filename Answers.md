### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
* Virtual Machines and Docker containers both, isolate an application and its dependencies into a self contained unit that can run anywhere, and
remove the need for physical hardware.
* A Virtual Machine is basically a stimulation of a real computer. A VM provides hardware virtualization. VM's use a hypervisor.
* Docker Containers share the host sysytem's kernel with other containers so, you cannot run a container with a guest operating system that differs from the host. They are smaller then VM's and start up faster. There is no need for a hypervisor. 

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
* `49160:8080` specifies that you are mapping port `8080` to the host machine port`49160`.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
*The main purpose of using a "container orchestration platform" is to automate the arrangment, coordination, and management, of containers.


4. How do you change the number of replicas in a Kubernetes cluster?
*The number of replicas in a Kubernetetes Cluster can be changed by finding "specs" in  the deployment.yml file, and changing the number to the desired number of replicas.

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
* Horizontal scaling means you add more machines( only limited by how many entities can be connected). Vertical scaling means you add more power(CPR,RAM) to an exising machine(limits are defined by hardware).

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
* The `free` tier of containers on Heroku- allow you to experiment with your own projects while the paid tiers can handle larger amounts of traffic to your application.