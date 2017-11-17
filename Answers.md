### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)  

1. ## _Container v Virtual Machine_
   | Virtual Machine | Container |  
   | ----------------|-----------|  
   | Server virtualization | OS virtualization|  
   | Runs its own operating system | Runs in different server environments |
   ----------------------
   Containers sit on physical server's and the host operating system and shares components.  It allows applications to be packaged with their dependencies rather than depending on an entire virtual machine to contain them.
  
2. ```  $ docker run -p 49160:8080```  
In this case, 49160 refers to port 49160 of the local machine, and 8080 refers to port 8080 inside the container.  The command maps them together.

3. Container orchestration platforms allow for the automation of certain tasks such as resource management,m scheduling, and managing services to scale software as necessary.

4. The number of replicas in a Kubernetes cluster can be changed by modifying the configuration files.

5. **Horizontally**: Using more servers to meet demand  
**Vertically**: Allocating additional resources on existing servers to meet demand.

6. The free tier of containers on Heroku go to sleep after half an hour of inactivity, and they require a certain amount of inactivity per 24-hour period and impose limitations on the active hours available per month.  The paid tier does not have this limitation and also includes additional resources compared to the free tier.