### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
1. Describe the differences between a Docker container and a virtual machine.
  - Docker Container: an optimized VM that reduces container 
    bloat at the cost of roughly 97% performance speed.
  - Full Virtual Machine: better sandboxing and tools at the cost
    of more resources per image.
2. What makes a container more aptly-suited for portability?
  - Because they are stripped down they have a small file size
    and can be used with various plug-ins depending on the
    inidividual's needs.
3. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
  - Redirects port 8080 from the container to the host's 49160 
    port.
4. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
  - To deploy across multiple containers.
5. How do you change the number of replicas in a Kubernetes cluster?
  - kubectl scale (fastest)
6. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
  - Scaling Horizontally: increase server load, often by distribution.
  - Scaling Vertically: increase disk space.
7. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
  - The dyno types (distributed server nodes).
  - The resources the dynos use (paid = more/better):
    - CPU and computing
    - RAM
    - Mixed dyno setups
    - Pro features:
      - horizontal scaliablity
      - app metrics
      - preboots
      - autoscaling
      - always-awake (free dynos sleep for 30 min due to 
                      inactivity)
    
