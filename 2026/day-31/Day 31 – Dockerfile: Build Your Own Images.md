#  Task 1: Your First Dockerfile

Create a folder called my-first-image

Inside it, create a Dockerfile that:

Uses ubuntu as the base image

Installs curl

Sets a default command to print "Hello from my custom image!"

Build the image and tag it my-ubuntu:v1

Run a container from your image

Verify: The message prints on docker run
### Creat first folder
my-first-image
### create dockerfile
vim dockerfile
### build image
docker build -t my-ubuntu:v1 .       where  [-t my-ubuntu] is image tag and [v1] means version and [.] means current folder
### run container
docker run my-ubuntu:v1

<img width="1366" height="768" alt="Screenshot (267)" src="https://github.com/user-attachments/assets/aeaf1e2d-e068-4004-b145-2265886a79cd" />

# Task 2: Dockerfile Instructions
Create a new Dockerfile that uses all of these instructions:

FROM — base image

RUN — execute commands during build

COPY — copy files from host to image

WORKDIR — set working directory

EXPOSE — document the port

CMD — default command 
