# list all containers:
docker ps -a

# to check all the running containers:
docker ps

# to stop any container
docker stop <container_id>

# To create new image:
docker build -t <app_name> .

# To run image in container, use below command
docker run -d -it node:latest

# To run image from command line
1. docker run --name <app_name_for_container> -p <COMPUTER_PORT>:<IMAGE_PORT> -d(for detach) <actual_image_name>

# In order to sync local folder to container:- (-v stands for volumns to sync local folders)
  1. install a nodemon server in docker file
  2. docker run --name myapp_c_nodemon -p 4000:4000 -d --rm -v D:\git\docker-crash-course\api:/app -v /app/node_modules myapp:nodemon

# To start cotainer of docker-compose file
  1. docker-compose up

# To end cotainer of docker-compose file
  1. docker-compose down

# To remove images and volumns docker
  <!-- 1. docker-compose down --rmi  all (to remove all images) -v (for volumns) -->
  1. docker-compose down --rmi all -v

# To remove all instance of images and container, use below command
docker system prune