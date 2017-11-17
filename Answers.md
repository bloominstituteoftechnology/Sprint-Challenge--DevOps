#Answers

1) A docker container runs on a bare minimum linux environment which sets on top of a normal OS.  Containers cut out a big chunk of overhead of a typical VM.  Since containers have smaller file size they can be ftp-ed easily over a network, along with being executed quickly in easy commands (e.x. docker run).

2) the -p tells what port to access your app on your container. <host port>:<container port>

3) It helps analyize/monitor/schedule container and instances.  Configure container settings.  Start and stop containers.  Scale them with more ease.

4) Looks like you can specify it in the yaml file?

5) To scale veritcally means to add more capacity/resources; disk spaces, CPU, bandwith etc..  Scaling horizontally means to add more software/code and to connect software components.

6) The main difference looks like the amount of process you get and the amount of tooling, features, and metrics.