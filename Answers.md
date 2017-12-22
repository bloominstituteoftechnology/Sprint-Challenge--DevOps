### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

The VM is just a raw OS and it does not contain any custom software that is required to run a server/program. Docker container is 'prepackaged', in the sense, it contains the host OS, dependent libraries as well as your custom business logic. If you use a virtual machine, you'll have to first set it up and then install, or import the necessary softwares, followed by your actual application. This process can be cumbersome and could be erroneous, since it involves manual work.
On the other hand docker is just an image, with a single docker run command, all of the steps mentioned above are automatically executed.

2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
The internal port 8080 in the container is exposed as 49160 to the external world. 

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
The purpose of using a container orchestration platform is to keep multiple containers running simultaneously. Its also used for fault tolerance, so when containers go down, it brings up a new instance.

4. How do you change the number of replicas in a Kubernetes cluster?
kbntes scale --current-replicas=<+/- scale number>

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

horizontally= create more instances of the same application.
vertically= add more processors/resources to an existing application.

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
The paid tiers keeps your applications running (as long as you pay :) ).