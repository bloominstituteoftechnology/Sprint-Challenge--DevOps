### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

DevOps and Deployment Assessment

1.Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

As stated below, a container is just a mini-virtual machine with a stripped down OS with nginx inside which can then run on any machine, platform-agnostically. It is simpler to deploy since in many cases the VM is only doing one simple set of tasks that does not require the "full" capabilities of a VM, so you can use a container for this and thus free up machines for running other things. Also, there is a large amount of pre-built Docker images which can be used to get things rolling. Sometimes one line of code is all that is necessary to download, install, and spin up an instance just like you would a VM template. 


2.Given the commend docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>, what does 49160:8080 specify?

The application is listening on port 8080. If you type some IP address in your browser(example: like 192,168.99.100): 49160, your website should activate. It is mapping the container's port over to 49160 where it is hosted. 


3.What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?


A container is just a mini-virtual machine with a stripped down OS with nginx inside which can then run on any machine, platform-agnostically. Kubernetes, for this example, lets you deploy and manage containers to clusters of virtual machines so that you can keep track of them all, not get charged for wasting server overhead on abandoned containers, etc. Although it is a Google product, it works with a wide variety of cloud platforms, hypervisors, OS instances, etc. You can manage everything from one spot, one command line.

4. How do you change the number of replicas in a Kubernetes cluster?

You can use Replication Controller, Replica Sets, or the preferred way which is deployments.

 
Use the Kubernetes Downward API for this. Create a file, let's say deployment.yaml. Add something like

apiVersion: extensions/whateverversionidentifier
kind: Deployment (this could be ReplicationController or Replica Set if you do it that way)


metadata:
  name: blahblah (this is the name of your Replication Controller
spec:
  replicas: number of replicas here
  template:
    metadata:
      labels:
        app: same name as blahblah above
    spec:
      containers:
      - name: blahblah
        image: namegoeshere/blahblah
        ports:
        - containerPort: whichever port number goes here

When you have all that, do this:
# kubectl create -f rc.yaml
replicationcontroller "blahblah" created

Or, to do a deployment, run 
# kubectl create -f deployment.yaml
deployment "blahblah" created

To do it as replica sets, you would do it like:
#kubectl create -f replicaset.yaml
Then # kubectl describe rs blahblahrs

use # kubectl get pods to see what you have that is running

If you describe it with something like 

# kubectl describe deployment blahblah

then you will have name, namespace, timestamp etc, number of replicas and an entry for new Replica Set will have blahblah-somenumberhere.

When you identify which pod will be hit with a particular request in PHP, using 
#echo "Pod ".$_SERVER['POD_NAME']." for example, then in the API you pass it in here:

spec:
      containers:
      - name: blahblah
        image: etc etc
        ports:
        - containerPort: 80
env:
        - name: POD_NAME
          valueFrom:
            fieldRef:
              fieldPath: metadata.name



Then you do 

#kubectl delete deployment blahblah

#kubectl get pods
Then 
#kubectl create -f deployment.yaml

then you expose the pods to external network requests:

# kubectl expose deployment blahblah --port=80 --target-port=80 --type=NodePort
Then # kubectl describe services blahblah

This will show you what port it is listening on, which it is forwarding to port 80 of the containers.

To change the number of replicas manually, do
# kubectl scale --replicas=TYPE NUMBER OF REPLICAS HERE deployment/blahblah

Or, you can change their label:
# kubectl label pods blahblah-10digitnumbergoeshere-someadditionalidentifer app=notblahblah --overwrite

You can use the --all flag after pods to change them all but if you have changed any individual labels you will need to delete them separately since deleting the deployment will not remove them, as they were 'reassigned' by the label change. 


5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

Increasing the number of containers of the service is considered making it to be “horizontally scalable”. A horizontal deployment deploys and promotes only a single application. Dependencies are provided somewhere else. For a team following the github flow, for example, the initial branch, the pull request and finally the merge should represent stages in the horizontal progress toward production-ready code. This also has the advantage of catching most integration problems in the development and QA stages, because production-ready code can make it more quickly into the integration tier and is immediately available to any integrating applications.

A vertical deployment is one that requires deploying all tiers and components in order to test any one of them. This increases the complexity and resource footprint required to develop an application. Work done on other components or tiers in the stack are not available until the vertical development deployment is refreshed.


6. Differences between paid and free heroku tiers

Now, in heroku, the free dynos are allowed 18 hours awake per 24 hour period. You can build apps using both 1 web and 1 worker dyno as well as heroku run and the scheduler, get more usage per app and never receive a surprise bill, and dynos can have custom domains.


> Written with [StackEdit](https://stackedit.io/).
