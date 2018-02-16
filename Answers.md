# Answers.md

## Questions

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
1. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
1. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
1. How do you change the number of replicas in a Kubernetes cluster?
1. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
1. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

---

## Answers

1. A virtual machine creates a Linux sandbox with resources allocated to it. After proper configuration _can_ have the same enviroment as the production server (Assuming a proper provisioning script).<br/>With Docker you push an inert, imutable file as a snapshot of your production code called an image. The `run` command creates an instance of the image as a protable encapsulation of the image called a container. Docker containers shares resources across multiple containers.Docker images are stored in a repository and all configuration changes are held in a seperate writable layer which is discarded when the container is no longer running.<br/>**TLDR**: Virtual machines provide an isolated, resource heavy enviroment which still has to have proper provisioning to over come the _it works on my machine_ conundrum. Docker containers are a light weight instance of your production code which also allows easy access to the production instance as all images are cloud based.
1. `49160:8080` maps between the container port `8080` and a port on the local machine `49160`.
1. Kubernetes in particular provides automating deoployments, scaling and distributing operations of application containers, load balancing, zero-downtime deoploys.
1. `kubectl scale --replicas=[number] [replicaset name]`
1. "vertical scaling" is improving the power and resources of your exististing network.<br/>"horizontal scaling" is adding aditional machines to your network.
1. horizontal scaling/auto scaling.

---

## Notes

**Your responses to the short answer questions should be laid out here using markdown.**

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)