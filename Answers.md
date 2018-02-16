### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

Docker provides OS-level process isolation which best suits packaging portable and modular software. Virtual machines offer isolation at the hardware abstraction layer.

### 2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

hostPort:containerPort

### 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

Container Orchestration refers to the automated arrangement, coordination, and management of software containers. Automated deployments, scaling, and operations of application containers across clusters of hosts while providing a container-centric infrastructure are just some of the features provided by a container orchestration platform. These features mitigate bottle necks caused by software growth through out it's development life cycle.

### 4. How do you change the number of replicas in a Kubernetes cluster?

A ReplicaSet can be easily scaled up or down by simply updating the .spec.replicas field in frontend.yaml and submitting it to a Kubernetes cluster. The ReplicaSet controller ensures that the desired number of pods with a matching label selector are available and operational.

### 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Vertical scaling can essentially resize your server with no change to your code. It is the ability to increase the capacity of existing hardware or software by adding resources. Vertical scaling is limited by the fact that you can only get as big as the size of the server.

Horizontal scaling affords the ability to scale wider to deal with traffic. It is the ability to connect multiple hardware or software entities, such as servers, so that they work as a single logical unit. This kind of scale cannot be implemented at a moment’s notice.

### 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

# Pricing | Heroku

## Hobby

$0 — $9 prorated to the second You pay only for the time your database is provisioned as a fraction of the month. E.g. in a 30 day month having it provisioned for 2 days will cost you 1/15th of the list price.

## Standard

* Continuous Protection
* Performance Analytics
* Fork / Follow
* 4 days rollback
* Max 1 hour downtime / month

$50 — $3,500 prorated to the second You pay only for the time your database is provisioned as a fraction of the month. E.g. in a 30 day month having it provisioned for 2 days will cost you 1/15th of the list price.

## Premium

* Standard Tier Features
* HA Database
* Encryption at rest
* 1 Week rollback
* Max 15 minutes downtime / month

$200 — $6,000 prorated to the second You pay only for the time your database is provisioned as a fraction of the month. E.g. in a 30 day month having it provisioned for 2 days will cost you 1/15th of the list price.

[Heroku Pricing Source](https://www.heroku.com/pricing "Permalink to Pricing | Heroku")
