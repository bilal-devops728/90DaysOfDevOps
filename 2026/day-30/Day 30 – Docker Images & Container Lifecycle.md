# Day 30 – Docker Images & Container Lifecycle
# Task 1: Docker Images
Pull the nginx, ubuntu, and alpine images from Docker Hub.

List all images on your machine — note the sizes.

Compare ubuntu vs alpine — why is one much smaller?

Inspect an image — what information can you see?

Remove an image you no longer need.
###  we pull images of alpine,ubuntu,nginx
- and then we remove images.

 <img width="1366" height="768" alt="Screenshot (259)" src="https://github.com/user-attachments/assets/2e4d8bc3-bef2-4ba3-a716-e2057c875104" />
 
 ## now we inspect image and we get detailed internal information of image in JSON FORMAT.

 <img width="1366" height="768" alt="Screenshot (258)" src="https://github.com/user-attachments/assets/eab4850f-e749-42e7-9d43-3370ee21268b" />

 # Task 2: Image Layers

 Run docker image history nginx — what do you see?
 
Each line is a layer. Note how some layers show sizes and some show 0B

Write in your notes: What are layers and why does Docker use them?

- we use command docker image history nginx
- ### WHAT ARE IMAGE LAYERS?
-  The image  created combination of multiples layers dockerfile have instructions layer.Layers are only read-only.
-  docker used layer for speed.

    <img width="1366" height="768" alt="Screenshot (260)" src="https://github.com/user-attachments/assets/1dae0e52-8da3-45ce-902b-8ed36c09ff90" />

  # Task 3: Container Lifecycle
  Practice the full lifecycle on one container:

Create a container (without starting it)

Start the container

Pause it and check status

Unpause it

Stop it

Restart it

Kill it

Remove it.

## COMMANDS
### start the conatner
  docker start container_name
### stop conatiner
docker stop container_name
### restart container
docker rerstart container_name
### kill container
docker kill container_nmae
### pause container
docker pause container_name
### unpaused container
docker unpause container-name

<img width="1366" height="768" alt="Screenshot (261)" src="https://github.com/user-attachments/assets/aaa97236-9d13-49f3-b8f0-7e8955dd5d19" />

<img width="1366" height="768" alt="Screenshot (262)" src="https://github.com/user-attachments/assets/9d73edb4-ad22-4219-9f3e-9f2bee08a2cf" />

# ask 4: Working with Running Containers
Run an Nginx container in detached mode.

View its logs.

View real-time logs (follow mode).

Exec into the container and look around the filesystem

Run a single command inside the container without entering it

Inspect the container — find its IP address, port mappings, and 

### view logs
docker logs mynginx
### view live logs
docker logs -f container_name
### to go exec in container
docker exec -it mycontaner_name bash
### run single command without entring in container
 docker exec mycontaner_name ls /use/share/nginx/html

<img width="1366" height="768" alt="Screenshot (264)" src="https://github.com/user-attachments/assets/61709fe0-c653-4e4f-b132-b39b36d9bcdc" />

 <img width="1366" height="768" alt="Screenshot (265)" src="https://github.com/user-attachments/assets/011c8f53-d85e-4867-b48b-b2d4edf0416e" />


