
# Q&A for DevOps Sprint Challenge

## 1) Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

#### A Docker container runs in the host's OS which allows it to use the host OS resources. If you had a 1gb container image, in order to run a full VM you would need 1gb per the number of VMs desired. With Docker, the containers share the resources.

#### A full VM get it's own set of resources, with minimal sharing. You get more isolation, but it takes up more resources. Docker is less isolated, with much lighter use of resources. A full VM may take minutes to start, where as a Docker image can take less than a second. Containers are great for portability because since the share host OS resources, they can be deployed across multiple machines with minimal issues.

## 2) Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

#### This command binds port `8080` of the container to port `49160` of the host machine.

## 3) What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

#### An orchestration platform provides a degree of automation to the process of deploying multiple containers to implement an application. This is especially useful as the number of containers and hosts grows.

## 4) How do you change the number of replicas in a Kubernetes cluster?

#### To change the number of replicas in a Kubernetes cluster, you would use the command `kubectl scale --replicas=3`, which in this case would set the number of replicas to 3.

## 5) What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

#### Horizontal scaling means adding more machines to your network to increase computing resources. Vertical scaling, on the other hand, increases resources by upgrading the computing power of the current machine.

## 6) Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

#### Heroku's paid tiers allow for advanced metric tracking, multiple workers and an "always on" application. Their free tiers, by comparison, are set to sleep after 30 minutes and only allow a single worker.