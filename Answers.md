### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

1. The benefits of containers often derive from their speed and lightweight nature; many more containers can be put onto a server than onto a traditional VM. VMs and Containers differ on quite a few dimensions, but primarily because containers provide a way to virtualize an OS in order for multiple workloads to run on a single OS instance, whereas with VMs, the hardware is being virtualized to run multiple OS instances. Containers’ speed, agility and portability make them yet another tool to help streamline software development


2. 49160 - docker container port 
   8080 - host 

3. Containers need management. These tools provide:
- Provisioning
- Configuration scripting
- Monitoring
- Rolling upgrades and rollback
- Service discovery

4. kubectl scale [--resource-version=version] [--current-replicas=count] --replicas=COUNT (-f FILENAME | TYPE NAME)

5. A 'vertical' deployment is one that requires deploying all tiers and components in order to test any one of them.
A horizontal deployment is one that focuses only on one component or tier. 

6. If an app has a web dyno, and that web dyno receives no traffic in a 30 minute period, the web dyno will sleep. Paid one will not.