### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. VMs require a bootable complete operating system with pre-selected limits on memory and disk space.   Docker containers require only the memory and disk space of each container and share the host's operating system.  Docker containers run Linux, VMs can be any operating system compatible with the hardware and VM application.

2. `-p 49160:8080` Maps the Docker Container's port 49160 to host port 8080.

3. To run multiple Docker Containers in an application - including clients and servers.

4. In the gui edit the `desired-replicas` and `max-replicas` fields
 ![Editing YML] (https://photos.google.com/archive/photo/AF1QipM6O9DASgOAhh9n_sTkIVpJn-eAbJ5hG0dR58xL)
 , on the command line edit the "replicas" field in an editor and execute `kubectl create -f [yaml filename] --record`

5. In horizontal scaling addition servers are linked in to share the load, in verticle scaling a server's capibilities are improved.  [IBM Explanation](https://www.ibm.com/blogs/cloud-computing/2014/04/explain-vertical-horizontal-scaling-cloud/)

6. The Heroku free tier limits usage to 1000 hours/month and autosleeps after 30 minutes of inactivity, all the paid tiers have unlimited hours and never sleep.  The alternative major difference is that the least expensive paid tier is $7/month while the free tier is free.

