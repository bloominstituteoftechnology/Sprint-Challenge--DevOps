### Your responses to the short answer questions should be laid out here using markdown.

For help with markdown syntax, [go here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


# Assessment Questions 

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
  * The main difference between a Docker container and a VM is that containers work in a different scope than VMs. Containers have only just what you need to test out an App in a controlled environment. Because Containers use only what you'd need to test an app, it uses much less resources than a VM that has to boot up a full copy of an OS, a bunch of apps, binaries, Libraries and etc. 

2. Given the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
  * 