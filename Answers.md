### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Describe the differences between a Docker container and a virtual machine. 

> Containers are an abstraction at the app layer that packages code and dependencies together.
> Multiple containers can run on the same machine and share the OS kernel with other containers,
> each running as isolated processes in user space. Containers take up less space than VMs
> (container images are typically tens of MBs in size) and start almost instantly.

> Virtual machines (VMs) are an abstraction of physical hardware turning one server into
> many servers. The hypervisor allows multiple VMs to run on a single machine.
> Each VM includes a full copy of an operating system, one or more apps, necessary binaries 
> and libraries - taking up tens of GBs. VMs can also be slow to boot.

* What makes a container more aptly-suited for portability?

> Docker abstracts away more networking, storage, and OS details from the application. With Docker, 
> the application is truly independent from the configurations of these low-level resources. When 
> you move a Docker container from one Docker host to another Docker-enabled machine, Docker 
> guarantees that the environment for the application will remain the same.

> A direct benefit of this approach is that Docker enables developers to set up local development 
> environments that are exactly like a production server. When a developer finishes writing and 
> testing his code, he can wrap it in a container and publish it directly to an AWS server or to 
> his private cloud, and it will instantly work because the environment is the same.

2. Given the command 
```
docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, 
```
* What does 49160:8080 specify?

> Here port 49160 of the host is mapped (bound) to port 8080 of the container.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

* Provisioning: These tools can provision or schedule containers within a container cluster and launch them. 

* Configuration scripting: Scripting permits you to load your specific application configurations into containers. 

* Monitoring: The container management tools track and monitor containers’ health and hosts in the cluster. The tools also run system health checks and report irregularities with the containers, the VMs they live in and the servers on which they run.

* Rolling upgrades and rollback: When you deploy a new version of the container, or the applications running within the containers, the container management tools automatically update them across your container cluster. If something goes wrong, they enable you to roll back to known good configurations.

* Service discovery: In old-style applications, you need to spell out explicitly where the software can find each service that’s required to run. Containers use service discovery to find their appropriate resources.

* Container policy management: Where do you want containers to launch? How many should be assigned per CPU? All these questions and more can be answered by setting up the correct container policies.

* Interoperability: Containers should work with your existing IT management tools.

4. How do you change the number of replicas in a Kubernetes cluster?

> You can change the number of replicas in a Deployment Specification File (.yml)

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

> To scale horizontally means to add more nodes to (or remove nodes from) a system,
> such as adding a new computer to a distributed software application. An example  
> might involve scaling out from one Web server system to three. System architects 
> may configure hundreds of small computers in a cluster to obtain aggregate 
> computing power that often exceeds that of computers based on a single traditional 
> processor. Size scalability is the maximum number of processors that a system can accommodate

> To scale vertically means to add resources to (or remove resources from) a single node in a system,
> typically involving the addition of CPUs or memory to a single computer. 

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

> with free tier of heroku:

 * domain name has 'herokuapp'
 * you can't deploy more than 5 apps
 * it will sleep your app when it is not in use.
 * size limitations 
 * etc.