
# Assessment Answers
 ### 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
    Docker containers use a lot less resources and generally run faster than VMs. Dockers also don't have system overhead to worry about.

 ### 2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
    `49160:8080` is the port number used for the application.

 ### 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
    It helps when scaling a huge application and getting a good division of power and optomization.

 ### 4. How do you change the number of replicas in a Kubernetes cluster?
    Either let it autoscale or update .spec.replicas

 ### 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
    Horizontally means adding nodes or even adding more servers. Vertically means increasing one computer/server's CPU or memory.
 ### 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
    The free one sleeps after only 30 minutes of no activity and is limited to just one worker.