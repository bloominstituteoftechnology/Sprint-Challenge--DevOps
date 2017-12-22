# Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
*Docker and VMs are similar. The biggest difference is that Docker is a specific container designed to deploy and run one single particular application, while VMs are made to virtualize technology so that a user can run a lot of different softwares or processes (usually from a different OS than the host system).*

# Given the commend docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?
*49160:8080 tells Docker to bind port 8080 of the container to port 49160 for access to the application. If you ran an image with these settings, your container would be available at URL:49160*

# What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
*The top 3 container management platforms are Docker Swarm, Kubernetes, and Mesoshpere. They're all good at what they do and they're widely popular, and they have different strengths and weaknesses and a lot comes down to preference and the way you'd like to orchestrate your containers, but they're all very important to making the most out of containers. In short, the features that they all share are:*

*Provisioning: provisioning can schedule containers within clusters to launch them, and make sure they're in the best VM based on certain requirements you may have
Congifuration and Scripting: allowing you to load specific application configs into the containers), Monitoring (self explanatory, tracks and monitors the health of the containers and restarts containers if they fail,
and Rolling upgrades and rollbacks: whenever you deploy new versions of containers, the management tools will update them across the cluster for you, and vica v if something goes wrong you can rollback cluster-wide*

# How do you change the number of replicas in a Kubernetes cluster?
*I'm not 100% on this answer, but based on the kubernetes documentation it seems that you can just specify the number of replicas in the configuration. There's a replicas field that goes into every .yaml manifest. In the docs you create an example `frontend.yaml` file. If you want, you can set it to scale automatically horizontally by using Horizontal Pod Autoscalers in `hpa-rs.yaml`. This allows your server to grow in replicas without manually adding more*

# What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
*To put this into only a few words: Scaling up, vertically, is to add more power to existing machines, while scaling horizontally is adding more machines in total to the power pool. When there's a lot of congestion on a highway, the city or state or whatever governing body will scale that highway horizontally, as in just make the highway wider, to allow more cars. When there's a busy restaurant inside New York City, they vertically scale by setting up extra chairs and tables for patrons, since you cannot immediately add extra space to the restaurant, they just make the best use of what they already have to accomodate their guests.*

# Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
*As you scale up in price, Heroku offers more robust and powerful features per plan. The main difference is the amount of allotted power and bandwidth (RAM, CPU, etc) being dedicated to your project. Additionally, as you climb up in tiers they begin to offer simple horizontal scalability and autoscaling as your service grows on their platform.*
