### docker commands





```bash
apt install docker.io

nano /etc/apt/sources.list

apt install docker.io

apt remove docker.io

docker pull nginx

docker images	//to view all images

docker ps //to view the running cnatainers

docker ps -a //to view all cnatainers

docker run nginx //to run nginx image (now you are inside a container)

docker run --name <any_container_name> -p 4000:4000 <image-name> // <port that we will map to the 
container >: <port exposed by the container>

docker stop <ContaierID OR name>		

docker build -t myapp . // dot is a relative path to the docker file from the dir in cmd

docker image rm <image_name> //remove image (must not used by any container)

docker image rm <image_name> -f	//remove image by force

docker container rm <container_name> //remove container

docker system prune -a //remove all images,containers and volumes

docker build -t myapp:v1 . //build image with new tag name V1 (version 1)

docker run --name <any_container_name> -p 4000:4000 <image-name>:v1 //run version 1 of the image

docker build -t myapp:nodemon	.

docker run --name <myapp_c_nodemon> -p 4000:4000 --rm -v <project-folder-path>:<folder-mappedToTheContainer (/app)> -v /app/node_modules <image-name>:nodemon

docker-compose up

docker-compose down --rmi all -v // --rmi all -v to delete images and volumes
```





