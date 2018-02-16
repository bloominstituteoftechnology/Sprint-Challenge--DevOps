1. A Docker container is an optimized version of a Virtual Machine that contains just enough parts to run your application. Because of this, the Docker container is faster and uses less system resources.

2. The left port is the port of the host that will be accessed and the right port is the port of the container. 

3. Container platforms will allow for automatic scaling of an application based on the demand of the application. Whether the demand is slowly increasing over time or there is a sudden spike in traffic, a container platform should be able to automatically scale and handle the workload.

4. `kubectl scale --replicas={number of replicas}`

5. Horizontal scaling is an increase in the number of machines running the application. Vertical scaling is upgrading the hardware of existing machines running the application.

6. Free heroku containers cannot scale and will go to sleep after not being used for 30 minutes, meaning that it will take a while to start back up when it is accessed again. Paid heroku containers stay awake, allow for scalability, and allow for more dyno hours.