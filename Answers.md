### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Virtual machines include their own copy of an operating system. This provides isolation between the virtual machines, 
but the overhead of the operating systems can make virtual machines take up a lot of resources. Containers do not 
include an operating system. They share the host operating system with other containers, relying on the docker engine to abstract 
away the details of the host operating system. This allows containers to take up less resources, so a single server can run many
more containers than it could virutal machines. 

2. The 49160:8080 means that port 8080 of the container is bound to port 49160 of the machine running the container. For example,
if the docker container is running the httpd service on port 8080, it can be accessed on the host at port 49160. 

3. Container orchestration platforms such as Kubernetes or Docker Swarm make it easier to manage applications that consist of 
a large number of containers. For example, Kubernetes includes a Horizontal Pod Autoscaler, which can automatically adjust the number 
of containers that are running based on resource utilization. If a CPU is close to 100% utilization due to a traffic spike, the 
Horizontal Pod Autoscaler will deploy more containers to deal with the traffic. When the the traffic subsides, the extra containers
will be deprovisioned to reduce costs.

4. The the number of replicas in a Kubernetes cluster can be configured using the command `kubectl scale`. For example, the command
`kubectl scale --replicas=4 rc/foo` will ensure that there are 4 replicas of the replication controller named foo running. It can also be changed
by updating the spec.replicas field in the configuration file.

5. Horizontal scaling entails running an application on more computers. Vertical scaling means to add more resources, such as
more RAM or a faster CPU, to an existing computer. An important advantage of horizontal scaling is that it is easier to dynamically
scale an application according to traffic patterns. For example, during high traffic periods, more virtual machines can be provisioned to run
an application. When the traffic subsides, these virtual machines can be deprovisioned to save on costs. 

6. Heroku calls their containers dynos. Heroku provides a free tier and a series of paid tiers for their dynos. The paid tiers include additional features, including more RAM, autoscaling, more granular application metrics, and the ability to run on dedicated hosts.

