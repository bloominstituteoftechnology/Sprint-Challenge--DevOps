## DevOps
### Sprint Assessment

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

    **Answer:**  
    A **Docker container (Container)** is an optimized version of a **Virtual Machine (VM)**. A Container runs on top of Docker engine, whereas A VM runs on top of a kernel. Container loads only the modules and packages needed to run the application. On contrast to VM, the Container do not require an Operating System. Therefore, Containers are faster and better in performance than VM's.

---

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

    **Answer:**  
    `49160` is the port at the localhost (`localhost:49160`).  
    `8080` is the port at the public server (`<PUBLIC_IP>:8080`).  
    `-p` is an alias for `--publish`, an option in **docker** command line.  
    `-p 49160:8080` part of the command tell docker to connect `localhost:49160` to `<PUBLIC_IP>:8080`.

---

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

    **Answer:**  
    Container Orchestration Platforms manages the scaling of containerized application. We can use **docker** to containerize. And we can use **Kubernetes** or **Docker Swarm** to manage those containers.

---

4. How do you change the number of replicas in a Kubernetes cluster?

    **Answer:**  
    The number of replicas can be specified in Kubernetes deployment configuration file (.yml file).

---

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

    **Answer:**  
    Scaling an application means adding more instances of the application on the server, in order to meet deployment needs. Horizonal scaling refers to changing (increase) the number of machines (server/hardware).  
    Vertical scaling refers to changing (increase) the software/hardware specs on the server machine.

---

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

    **Answer:**  
    The free tier limits the number of active hours (called dynos) per month and automatically sleeps after a period of inactivity. Maximum number of applications in free tier is limited to 5.

