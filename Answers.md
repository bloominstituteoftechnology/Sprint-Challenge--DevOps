## DevOps
### Answers to Sprint Assessment

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?



2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

    **Answer:**  
    `49160` is the port at the localhost (`localhost:49160`).  
    `8080` is the port at the public server (`<PUBLIC_IP>:8080`).  
    `-p` is an alias for `--publish`, an option in **docker** command line.  
    `-p 49160:8080` part of the command tell docker to connect `localhost:49160` to `<PUBLIC_IP>:8080`.

---

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?



---

4. How do you change the number of replicas in a Kubernetes cluster?

    **Answer:**  
    The number of replicas can be specified in Kubernetes deployment configuration file (.yml file).

---

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?



6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
