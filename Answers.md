1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

Answer: Docker container provides a way to virtualize an OS in order for multiple workloads to run on a single OS instance. whereas with VM, the hardware is being virtualized to run multiple OS instances. 

Docker images are stored in a repository, either the Docker Hub (a public set of repositories) or advanced features like Docker Data center, where images are stored in the Docker Trusted Registry. It’s easy to see how having an efficient distribution mechanism allows dozens, hundreds or even thousands of server hosts to run Docker images without having to download the entire image content each time code changes. This is particularly valuable when containers move around the physical infrastructure; getting the latest version of an application image needs to be achieved as quickly as possible.

2. Using the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

Answer: It specifies that the public port is redirected to a private port inside the docker container. 

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

Answer: When the application keeps growing and needs to be divided into smaller chunks as micro-services.
We now need a caching layer to increase performance, be able to process tasks asynchronously and quickly share data among the services. We will face some challenges like: service discovery, load balancing, secrets configuration, health checks, auto-scaling of containers, and zero-downtime deploys. The container orchestration platform is to provide automating deployments, scaling, and operations of application containers across clusters of hosts, providing container-centric infrastructure.

4. How do you change the number of replicas in a Kubernetes cluster?

Answer: We will have to write a yml file for deployment configuration. Inside the yml file, we will specify the replica numbers under the spec: replicas. And submitting this file to a Kubernetes cluster should create the defined ReplicaSet and pods that it manages using `kubectl create -f *.yml`.

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Answer: scaling horizontally affords the ability to scale wider to deal with traffic. It is the ability to connect multiple hardware or software entities, such as servers, so that they work as a single logical unit.
Scaling vertically resizes the server with no change to the code. It is the ability to increase the capacity of existing hardware or software by adding resources. it is limited by the fact that you can only get as big as the size of the server. 

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

Answer: free tier doesn't offer the auto-scaling, horizontal scaling, and zero-downtime deployment features that will boost the application performance tremendously.
