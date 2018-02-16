### Your responses to the short answer questions should be laid out here using markdown.
my references :
https://medium.freecodecamp.org/a-beginner-friendly-introduction-to-containers-vms-and-docker-79a9e3e119b
 https://medium.com/ingeniouslysimple/adopting-kubernetes-step-by-step-f93093c13dfe
  https://medium.com/google-cloud/kubernetes-101-pods-nodes-containers-and-clusters-c1509e409e16
For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

Containers and vm's abstract the physical harware where the application will run. The differences between the two is that VM's encompass a virtual OS which runs on the host machine and are administered by an application called hypervisor. Containers are more lightweight in that containers share a host OS kernel and are created and managed by the docker engine. Containers are relatively easy to create, launch quickly and can be intergrated with a wide range of docker images (prebuilt applications)

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

The whole line means docker take a specified docker image that runs on tcp port 8080 and publish on docker host

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

Containers allow us to build and ship distributed applications where machine constraints are abstracted away. Hoewerver even using containers there is still a significant amount of work to be done to deploy your application to a cloud provider. An applications needs scaling and remote disc persistance and this is where Kubernetes or Docker swarm come in and manages this for us. 
4. How do you change the number of replicas in a Kubernetes cluster?

Kubernetes doesn't run containers directly, instead wrapping them into a structure called a pod. Pods are used for replication in Kubernetes. You can change the number of replicas using the replication controller to make sure the number of pods specified are always up and available


5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Vertical scaling can essentially resize your server with no change to your code. It is the ability to increase the capacity of existing hardware or software by adding resources. Vertical scaling is limited by the fact that you can only get as big as the size of the server.
Horizontal scaling affords the ability to scale wider to deal with traffic. It is the ability to connect multiple hardware or software entities, such as servers, so that they work as a single logical unit. This kind of scale cannot be implemented at a moment’s notice.

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

the free heroku tier sleeps applications if they haven't been used after one hour, though there is a workaround for this (https://medium.com/@AndreyAzimov/how-free-heroku-really-works-and-how-to-get-maximum-from-it-daa53f2b3c57) , you only get 1000 hours of free  uptime per heroku account so if you have several applications this will be quickly eaten up. If you are using a static site use Netlify (no hour limits)

