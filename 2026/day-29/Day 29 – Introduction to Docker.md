# Day 29 – Introduction to Docker
Task 1: What is Docker?
Research and write short notes on:

What is a container and why do we need them?

Containers vs Virtual Machines — what's the real difference?

What is the Docker architecture? (daemon, client, images, containers, registry)

## What is docker?
Docker is open source centrlizad plateform designed to creat, deployment and run applications.docker is tool for deployment and used host o.s for containers.
dockeer allows to package an application with all his dependiences,runtime,all supporting softwears into one unit called containers so it run on every machine-
## Difference between container and virtual machines?
- virtual machines: Virtual machine is a virtual computer whhich have own operating system and run on host o.s and used dedicated resources from host hardwares directly.
- its architect is  HARDWARE>host os>hypervisopur>vm1,vm2,vm3
- these vm using dedicated resources from host H.W.
- ## WHAT IS CONTAINER?
- containers is advance version of virtual machines.
- Containers dont have own operating system.Container use all resources from host operating system not directly host H.W and used all resources on shared bases whenever container need resources they used host kernal for using host hardware resources.
- architecte is ## H.W>hostos>docker>container1,container2.
- or
- container is running instance of image and have all dependiences inculdes application code,libraries,enviroment etc.

## WHAT IS DOCKER ARCHITECTURE?
- Docker client: this is user interphase and we run all commands here like docker build, docker pull, docker run.The client send request to docker deamon.
- docker deamon: run in the background and performs actual works.functions are build images,run containers,manage volumes.
Client send request to deamon and deamon executed commands.
- Docker registory: this is place wehere all images are stored like docker hub.
 #  Task 2: Install Docker
- Install Docker on your machine (or use a cloud instance)
Verify the installation

Run the hello-world container

<img width="1366" height="768" alt="Screenshot (250)" src="https://github.com/user-attachments/assets/134c66e8-333d-44f9-9135-fd6b0568419b" />

<img width="1366" height="768" alt="Screenshot (252)" src="https://github.com/user-attachments/assets/4c712f7a-dc3f-4d9a-a2a0-ed926b69c131" />

# Task 3: Run Real Containers

Run an Nginx container and access it in your browser

Run an Ubuntu container in interactive mode — explore it like a mini Linux machine

List all running container

List all containers (including stopped ones)

Stop and remove a container

<img width="1366" height="768" alt="Screenshot (253)" src="https://github.com/user-attachments/assets/d57c7cdb-d894-427f-8d8a-c09b0562c26f" />

<img width="1366" height="768" alt="Screenshot (254)" src="https://github.com/user-attachments/assets/50409770-4942-4e2d-ad90-6f1f1f4c3043" />

# Task 4: Explore

Run a container in detached mode — what's different?

Give a container a custom name

Map a port from the container to your host

Check logs of a running container

Run a command inside a running container

<img width="1366" height="768" alt="Screenshot (255)" src="https://github.com/user-attachments/assets/7047113b-2636-4d8f-9d3c-8845b4b3bc6d" />

<img width="1366" height="768" alt="Screenshot (256)" src="https://github.com/user-attachments/assets/3d89d798-b3f1-401a-8447-b9679615a795" />
