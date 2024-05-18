**Check Docker**

**Check docker version**

Docker --version





**Check Docker Status**

Docker ps





**Check running Instances**

Docker image ls





**Check available volumes**

Docker volume ls





**Run Docker Instance**

Run starter docker image

Docker run hello world





**Run basic docker image**

docker run -p 80:80 -d nginx





**Run docker image with persistent volume**

docker run -p 80:80 -v nginx_data:/usr/share/nginx/html -d nginx







**Run docker image using your own files within persistent volume**

Mount the same host container inside the docker container volume

docker run -p 80:80 -v /usr/share/nginx_data/html:/usr/share/nginx/html -d nginx

cd html

ls



**Create a basic html file**

Vim index/html



**Check specific docker persistent volume**

docker inspect nginx_data





**Delete Docker images**

Check

Docker images



**List all containers**

Docker containers ls -a





**Delete a single docker container**

Docker rmi <image>





**Delete all images**

Docker rm -f $(docker ps -a -q)





**Delete docker image**

Docker rm <name of image> or <container id>