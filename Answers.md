### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

# Assessment Answers
 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

`A VM is an entire OS packaged in with a development environment, a Docker Container is an image of the software needed for the development environment. This can run easily on the Docker engine, where it can fetch all necessary dependencies.  A VM is quite a large file (a few hundred MBS). Whereas a Dockerfile is quite a small file (1-5MBs). `

 2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

`49160 is the host port and 8080 is the docker port. "49160:8080" links the two ports together in a manner where anything going to port 49160 will be mapped / forwarded to port 8080  `

 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

`Container orchestration platform's enable you to manage docker images allowing scaling to be easier`

 4. How do you change the number of replicas in a Kubernetes cluster?

`Edit "replicas" value in the config file, the update the file. `

 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

`Scaling Horizontally = Adding more hardware, usually meaning adding more servers`

`Scaling Vertically = Increasing the usage of the current server / servers`

 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

`Heroku's free tier sleeps after 30 mins of inactivity, the paid tier does not`
