<!-- ### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) -->

## Answers


1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

  * Docker Container - is like a snapshot of your environment that allows others to interact with your code using the same environment. Since there are issues / interactions with different environments (states) you can't necessarily just port your code to another user. Their machine will have a different state than yours, and the code might not function.

    * The container captures everything about your environment and packages it up. Your code, runtime, system tools, libraries, settings are all placed into a container. You are then able to share this container with other people, to allow them to inspect or interact with your code, without the liability of the environment polluting the structure.

  * Virtual Machine - a virtual machine allows you to create a similar build to another machine, without actually having that machine. Ie. you could run a Linux box using a specific node version that is completely different from your Windows box hosting the virtual machine. Virtual Machines operate more on replicating the hardware environment, than the software environment, though that information is also included. 

    * Virtual Machines can be very large, and are frequently slow. While they give you access to that other environment, it can be at the cost of efficieny and productivity, not to mention the space requirements of the host system.


2. Given the command docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

  * docker 
    * initialize docker CLI
  * run 
    * run the following command in a new image
  * -p 
    * publish a container's port(s) to the host
  * 49160 
    * bind this port of the container
  * : 
    * to
  * 8080
    * this port on the host machine
  * -d
    * detach, run container in the background and print container ID
  * <your_docker_username>
    * identifies your account
  * /
    * route to
  * <your_docker_image_name>
    * specified image


3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

  * Largely speaking, they work to keep you up and running. You have multiple hosts which are running your application, which are a cluster. When you create a cluster you define a number of replicas, their network and storage resources, ports to the outside world, etc. 
  * Both Swarm and Kubernetes work to maintain the state you stipulate when you configure the cluster. Various nodes of a cluster handle different tasks, and the Orchestration Platforms work to schedule tasks, maintenance, upgrages in the most efficient way possible. 
  * OP's also endeavour to balance the nodes workload so no one node is responsible for too much. Should a node fail, the OP will move that node's tasks to another node, while bringing another node online to take up the failed node's workload.
  * Swarm is still in beta, but allows you to perform additional functionality within Docker. 
  * Kubernetes is an established service created by google which interfaces with a large number of other resources. It does require you managing another element, but has the benefit of 15-20 years of development at this point.


4. How do you change the number of replicas in a Kubernetes cluster?

  * Through the Replication Controller (equality based), Replica Set (selector and equality based), or Deployment Controller (declarative), as you have it defined. You can also use an autoscaler, which will add replicas as needed to handle the load.
    * in the Replica Controller: kubectl scale rc NAME --replicas=COUNT
    * in the Replica Set: .spec.replicas (will ensure the desired number of pods which match the label are available and operational)
    * in the Deployment Controller: 
        * kubectl scale deployment ngins-deployment --replicas=x
      * for horizontal scaling:
        * kubectl autoscale deployment nginx-deployment --min=x --max=x --cpu-percent=x
    * with an Autoscaler: 
      spec: 
        minReplicas: x 
        maxReplicas: x


5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

  * Horizontal scaling adds nodes to a distributed network. 
    * adding a computer
    * adding a webserver
    * reduces down time as you're adding resources to an existing pool of resources
    * can create issues as the complexity of the network increases
  * Vertical scaling adds resources to a single node.
    * upgrade the CPU
    * add memory
    * requires downtime as you must remove the resouce from the network in order to perform the upgrade
    * computers themselves are relatively cheap, so it can be a quick way of increasing your processing power


6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
  * number of processes
    * a greater number of processes allow the app to handle more requests concurrently
    * the free tier is really only for proof of concept, and is not a production environment
  * SSL
  * Metrics
  * Scaling at the professional levels
  ------

#### Resources

