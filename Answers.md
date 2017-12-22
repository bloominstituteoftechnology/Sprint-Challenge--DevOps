### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### 1.  Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
*Answer: a container allows to have multiple workloads in a single operating system instance while virtual machine allows for multiple operating systems.  Docker container also differ from virtual machines when it comes to speed, agility and portability.  A benefit for software developers.*

### 2.  Given the commend docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?
*Answer: the port 49160 specifies the client port and port 8080 specifies the container port.  Basically, a handshake between the client port (locally) and port 8080 which is the internet port.  When running the above command, you will be sending the docker image from client port 49160 to port 8080.*

### 3.  What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
*Answer: While deployment your application in the early stages can be simple and you might not need to use the container orchestration platform.  However, as many applications goes through changes such as additional features, or functionality.  Kubernetes or Docker Swarm comes in to make it less challenging by handling service discovery, load balancing, configuration and zero-downtime deployment.*

### 4.  How do you change the number of replicas in a Kubernetes cluster?
*Answer: When changing number of replicas prior to deploying the application, one must edit the .yml file to adjust the number next to replicas under spec:*

### 5.  What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
*Answer: Horizonal or parallel scaling is where containers in a application work independently of each other.  A simple addition with no configurations of any other files to keep the application functional.  Vertical or sequential scaling is where functionality is impacted when changing one or more container.  Configuation is required to among containers to ensure the application to work properly*

### 6.  Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
*Answer: The main difference between free and paid tiers for Heroku, is that the free tier would put your app to "sleep" after inactivity while your paid tiers would allow you to progress with hosting your application consistently and not wait 10-20 seconds for the application to load.*