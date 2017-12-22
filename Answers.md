### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


# Assessment Questions Answers Bonn W.

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
  * The main difference between a Docker container and a VM is that containers work in a different scope than VMs. Containers have only just what you need to test out an App in a controlled environment. Because Containers use only what you'd need to test an app, it uses much less resources than a VM that has to boot up a full copy of an OS, a bunch of apps, binaries, Libraries and etc. 

2. Given the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
  * `-p` stands for port and `49160:8080` maps the path between port 8080 on the container and a port on my local machine.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm? 
  * They allow us administrative abilities like scheduling patches and rolling out new features on the fly. Also something to do about scaling... TBC

4. How do you change the number of replicas in a Kubernetes cluster?
  * 

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
  * Vertical scalling allows us to increase the capacity of hardware/software without changing code. 
  * Horizontal scalling adds hardware/software to deal with traffic such as connecting multiple devices or pieces of software to function as a single logical unit.

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs the paid tiers?
  * 

*key*
**TBC** = To Be Continued