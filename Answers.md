### Your responses to the short answer questions should be laid out here using markdown.
1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?  
>A docker container is different from a virtual machine because it is leaner and specialized for a much smaller range of tasks. It is more aptly  
>suited for portability because it takes up far fewer resources to run.


2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?  
>49160:8080 specificies that 49160 will be how someone can reach the image of the item that was hosted on localhost:8080 in your docker image

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?  
>  These tools limit the amount of containers and resources being used according to the demand

4. How do you change the number of replicas in a Kubernetes cluster?  
>

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?  
>scaling horizontally implies additional servers, scaling vertically implies increasing the server use of a single machine.

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?  
>  the free containers on Heroku sleep after 30 minutes of inactivity while the paid ones do not

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
