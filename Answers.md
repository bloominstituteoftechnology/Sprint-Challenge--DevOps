## Questions

#### Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

* Docker is just a fancy way to run a process, not a virtual machine.
#### Using the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

* Docker runs processes in isolated containers. A container is a process which runs on a host. The host may be local or remote. When an operator executes docker run, the container process that runs is isolated in that it has its own file system, its own networking, and its own isolated process tree separate from the host.

#### What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

* Container orchestration programs—Kubernetes, Mesosphere Marathon, and Docker swarm mode—make it possible to manage containers without tearing your hair ...

#### How do you change the number of replicas in a Kubernetes cluster?

* By using scale?

#### What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

* Image result for what does it mean to scale vertically
Horizontal scaling means that you scale by adding more machines into your pool of resources whereas Vertical scaling means that you scale by adding more power (CPU, RAM) to an existing machine.

#### Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

Paid version Enhanced visibility, performance, and availability for powering your professional applications.

* ALL HOBBY FEATURES +
SIMPLE HORIZONTAL SCALABILITY
THRESHOLD ALERTS
PREBOOT
LANGUAGE RUNTIME METRICS
512MB OR 1GB RAM
Performance M L
Superior performance when it's most critical for your super scale, high traffic apps.

* ALL STANDARD FEATURES +
MIX WITH STANDARD 1X, 2X DYNOS
DEDICATED
AUTOSCALING
2.5GB OR 14GB RAM
∞ Process Types

$25 - $500 per dyno/month
prorated to the second

Free

* Ideal for experimenting with cloud applications in a limited sandbox.

* CORE PLATFORM FEATURES
SLEEPS AFTER 30 MINS OF INACTIVITY
USES AN ACCOUNT-BASED POOL
OF FREE DYNO HOURS
CUSTOM DOMAINS
512 MB RAM │ 1 web/1 worker

Free

