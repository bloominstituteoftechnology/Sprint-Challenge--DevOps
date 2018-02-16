# Answers to Assessment Questions

1. Containers are an abstraction of the app layer that packages code and dependencies together, while virtual machines are an abstraction of physical hardware turning one server into many servers. You can also run multiple containers on the same machine and share the OS kernel with other containers, allowing each to run as isolated processes in userspace. While you can run multiple virtual machines on a single machine utilizing something such as hypervisor, each VM includes a full copy of an operating system, more or more apps, and necessary binaries and libraries. Overall this allows containers to start almost instantly, while VMs can be slow to boot.

2. In the command docker run 49160:8080 are the ports we are connecting. The first port is the localhost port that mode server is running on, and the second port is the port that is being used on docker.

3. It allows you to "package" up your app to run on another server the same one it runs on your local machine. It allows you to easily transfer between other servers, spin the app up, suspend it, and turn it off. It overcomes the version issue that you may experience when using different setups. It also allows you to create a build pipeline that makes it faster to get your app up and running from your local machine.

4. You originally set the number of replicas in your yaml file, but you can also scale a replica set by updating the .spec.replics field. You can also setup autoscaling by setting a mixReplicas and maxReplicas number in the yaml. The cluster should then scale depending on CPU usage of the replicated pods.

5. Vertically scaling is when you resize the server by increasing the capacity of existing hardware or software by adding resources. It is limited to only being allowed to get as big as the server. Horizontal scaling on the other hand is the idea of adding additional hardware. This is not something you can do at a moment's notice, and takes more time.

6. The free app will spin down after 30 minutes, or if the app is not in use. They also limit the amount of processes you can run, while the professional ones have unlimited.
