# Answers
1. Question: Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?
    * Answer: Virtual Machine is a virtualized or simulated environment, they have their own individual operating system, usually takes a long time to set-up and get up and running. A docker container is also a virtualized environment however it runs in a kernel layer and it is easy to customize with a Dockerfile and starts up very fast. In general docker container take significantly less resources than vms.
2. Question: Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?
    * Answer: It runs a docker container on port 8080 and maps that port to an external port 49160, so on localhost:8080 the server can be seen running, and on ip address: xxx.xxx.xxx.xxx:49160 the server can be exposed to the net.
3. Question: What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?
    * Answer: Being able to clone multiple docker images and balancing the load on each one of them for best performance.
4. Question: How do you change the number of replicas in a Kubernetes cluster?
    * Answer: using a deployment.yml configuration file and setting the options inside the file, under spec: set the replicas: 'any number'
5. Question: What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?
    * Answer: Vertical scaling means usually adding more performance and memory and space to the same machine so it can handle the load. Horizontal scaling means adding more machines to handle the load instead.
6. Question: Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?
    * Answer: Free tier Heroku containers are put to sleep after some time without any use, and this means that they take time to start up upon getting a request to use again. Free tier usually have less ram and can only run 1 process, where paid can run multiple processes.

# Deployment of Personal Project
1. Front End: https://mnc-front.herokuapp.com/
2. Back End: https://mnc-back.herokuapp.com/

# Back End API Documentation: Only the User Authentication has been implemented.
# Dev Ops Notes:
1. Knex Configurations / Commands
    - knex init
    - knex migrate:make initial
    - inside: data/dbConfig.js change development to production when ready to deploy

2. Authentication Configurations
    - Change: config.js secret: before deploying final.

# API Endpoints: 
## Registration: 
### Request Type: POST
1. Navigate to /register
2. Provide a user object following this template:
```JSON
{
    "email": "test@email.com",
    "password": "1234"
}
```
3. Server will return the userID# if successful.
4. Server will return the following error if unsuccessful:
```JSON
{
    "errorMessage": "unable to register user. Already registered? Try to log-in instead!"
}
```

## Login:
### Request Type: POST
1. Navigate to /login
2. Provide a user object following this template:
```JSON
{
    "email": "test@email.com",
    "password": "1234"
}
```
3. Server will return an object like this one if successful:
```JSON
{
    "id": 7,
    "email": "test@email.com",
    "auth": true,
    "createdAt": "2018-02-13 19:40:33",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJleHAiOjE1MTg1NTQ5NjAsImRhdGEiOiJ0ZXN0QGVtYWlsLmNvbSIsImlhdCI6MTUxODU1MTM2MH0.ijuolir7q2nkMa50Td6JLNLqfkdmUn7t7tuh89oEb_M"
}
```
4. Server will return this error if unsuccessful:
```JSON
{
    "errorMessage": "User not Authenticated, Please log-in again!"
}
```

## List Users:
### Request Type: GET
1. Navigate to /users
2. Provide a JWT with the token that was given when the user logged in in the headers Authorization.
3. A list of users will be returned.
4. Server will return this error if unsuccessful:
```JSON
{
    "error": "Token invalid, please login",
    "message": {
        "name": "JsonWebTokenError",
        "message": "invalid signature"
    }
}
```

## Delete a User:
### Request Type: DELETE
1. Navigate to /users
2. Provide a user object like the one bellow:
```JSON
{
    "email": "test@email.com",
    "password": "1234"
}
```
3. Server will return 1 if the user was deleted successfully.
4. Server will return an error if it was unable to delete the user.

## Update a User's Password:
### Request Type: PUT
1. Navigate to /update
2. Provide a user object like the one bellow.
```JSON
{
    "email": "test@email.com",
    "password": "1234",
    "newPassword": "4321",
}
```
3. Server will return 1 if the user was updated successfully.
4. Server will return an error if it was unable to update the newPassword, or was unable to authenticate with the provided password.