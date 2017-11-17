### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Assessment Questions with Answers
 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

 A container is much smaller than a virtual machine, in terms of storage space and system resources that are required. Containers are able to simulate what an environment would be like if it was pulling only on the resources that it is expected to need.

 A virtual machine is an isolated environment that has all of the system resources the entire environment needs in order to function, but with that isolation comes a larger requirement in system resources. 

 2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

 49160:8080 signifies <localhost>:<port number>.

 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

 If your application already has multiple containers and continues to grow, it's going to be important to have an orchestration platform for them to maintain functionality, traffic, and limiting downtime as close to zero as possible.

 4. How do you change the number of replicas in a Kubernetes cluster?

 There is a command called "kubectl scale" that can be used like this:

 $ kubectl scale rc NAME --replicas=COUNT \
    [--current-replicas=COUNT] \
    [--resource-version=VERSION]

    Taken from the documentation at:
    https://kubernetes-v1-4.github.io/docs/user-guide/resizing-a-replication-controller/

 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

 Horizontal scaling means dedication of more machines to the task, whereas vertical scaling means adding more power to the specific machone


 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

 Heroku has free, hobby, and professional tiers for app deployment.

 The free tier offers 550 - 1000 hours of using the core platform features of Heroku, which are multiple deployment methods, automatic patching, unified logs, buildpacks, routing, dyno (heroku containers are called dynos) management and SSH. The heroku environment will go to sleep after 30 minutes of inactivity.

 Hobby level has all of this, minus the sleep period, plus aplication metrics and up the capability to accommodate up to ten process types. The cost is $7 per dyno per month.

 Standard professional level has all of this, plus horizontal scalability, threshold alerts, prebooting, and 512 mb to 1gb of ram. Performance Professional Level has the standard features, plus autoscaling, 2.5gb up to 14gb of ram. The cost is $25-$500 dyno per month.