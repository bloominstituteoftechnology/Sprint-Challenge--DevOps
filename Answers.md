## DevOps and Deployment Assessment
---

####  Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

>#### Virtual Machine
>A virtual macine is an emulation of a computer system that runs an operating system and applications.  You can run a completely different, guest OS on the same hardware.

>#### Docker Container
>A Docker Container is an executible package of a piece of software including everything needed to run it (code, tools, system libraries, etc) that always runs the same regardless of environment.  Containers isolate software from surroundings to reduce conflicts.  You don't have to allocate significant chunks of memory to a container because it doesn't have to run a whole OS.

---
####  Given the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

> This specifies the mapping between the port inside the container (`8080`) with a port on the local machine (`49160`).


---
####  What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

> These are used to manage containerized applications at scale.



---
####  How do you change the number of replicas in a Kubernetes cluster?

Still trying to figure this one out.  This is what I found so far:
>**Scaling Resources** <br/>
$ kubectl scale --replicas=3 rs/foo                                 # Scale a replicaset named 'foo' to 3
$ kubectl scale --replicas=3 -f foo.yaml                            # Scale a resource specified in "foo.yaml" to 3
$ kubectl scale --current-replicas=2 --replicas=3 deployment/mysql  # If the deployment named mysql's current size is 2, scale mysql to 3
$ kubectl scale --replicas=5 rc/foo rc/bar rc/baz                   # Scale multiple replication controllers

---
####  What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

> **Horizontal** &rarr; scale by adding more machines to your pool of resources
> **Verticle** &rarr; scale by adding more power (CPU, RAM) to an existing machine

---
#### Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

> **Free** <br/> &rarr; Is for experimenting with cloud applications in a sandbox.  Sleeps after 30 mins of inactivity. <br/>&rarr; Uses an account-based pool of free Dyno (their version of container) hours

> **Paid**<br/> &rarr; Different options to your needs (you can pay more based on size/needs of project) <br/> &rarr; Never sleeps <br/> &rarr; Free SSL & Automated Certificate Management for Custom Domains <br/> &rarr; Metrics <br/> &rarr; 512MB - 14GB of RAM