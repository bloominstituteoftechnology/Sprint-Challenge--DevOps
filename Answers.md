### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Assessment Questions
 1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
 * Deploying means placing the software app on an external server different from that on the local machine to test or debug the app. This allows the developers to see how the app functions on different enviroments similar to a production-ready software app.

 * Containers allow software apps to be placed in a 'box' that can be run anywhere (different operating systems). In contrast, a virtual machine also includes the operating system. The main advantage of a container is since it doesn't include the OS, the contents are smaller, making them more easily portable and able to run on any OS. 

 2. Given the commend `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
 * This command runs an image that was built using a Docker file.

 * The first number is the server port on the local machine and the second number is the server port specified by the software app.

 3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm? 
 * They allow the developer to manage, scale, and deploy containers. They handle much of the details (automatation) of deploying and updating clusters.

 4. How do you change the number of replicas in a Kubernetes cluster?
 * A replica is a copy of the software app. It's useful to have relpicas in case something happens to the original one or for testing different things out without overloading the original. I'm also thinking this can be helpful for version control?

 * The number of replicas can be updated/changed by using the .spec.replicas field in the yml file. This is known as scaling the deployment. To apply the changes after scaling, the changes can be applied using 'kubectl apply -f deployment.yml'.

 5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
 * A horizontal scaling allows more nodes to be added to app. This is the method to add things such as more servers.

 * A vertical scaling meaning more things are added/removed to the single existing node. There is a limit to scaling vertically, whereas there isn't a similar limitation on scaling horizontally.

 6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
 * For paid tiers there's many more options that the developer can implement (such as horizontal scaling), while with a free tier there's a limit. With the free tier on Heroku, much of the work is done by behind the scenes by the platform. With Docker, there is more flexibility in what one can do, but this also means the process is more complex.