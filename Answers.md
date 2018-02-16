### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. Containers and virtual machines are two ways to deploy multiple, isolated services on a single platform. The difference between the two is that the container's system needs an underlying operating system that provides the basic services to all of the containerized applications using virtual-memory support for isolation.  VMs on the other hand have their own operating system using hardware VM support. VMs are managed by a hypervisor and utilize VM hardware, while containersystems provide operating system services from the underlying host and isolate the applications using virtual memory hardware. Since VMs mimick an actual machine, it needs to be booted up when ever you use it. This process takes some time whilsts a virtual machine starts up almost instantaneously because it doesnt need a whole booting process. This makes a container a lot more light weight or portable than vitual machines.

2. The -p 49160:8080 bit specifies the mapping between the port 8080 inside the container with a port on your local machine, in this case 49160.

3. Container orchestration platforms like kubernetes manages containers by giving a means to do deployments, an easy way to scale and monitoring of containers.

4. To increase or decrease the number of pods under a replication controller’s control, It is done using the ```kubectl scale``` command
```$ kubectl scale rc NAME --replicas=COUNT \
    [--current-replicas=COUNT] \
    [--resource-version=VERSION]
```    

5. Horizontal scaling means that you scale by adding more machines into your pool of resources whereas Vertical scaling means that you scale by adding more power (CPU, RAM) to an existing machine.

6. The Paid tier keeps your application awake, giving free SSL and Automated certificate management for custom domins, multipleworkers for more powerful apps, horizontal scalability, Threshold alerts, prebooting, and a larger storage RAM.