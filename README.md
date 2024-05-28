# Docker1
This is a simple project in which you can create your own customized Docker image to host a static webpage. You can also launch a docker container with your image inside it and store it in dockerhub.


You will need your AWS account if you want it to push to ECR, DockerHub Account, basic understanding of HTML and an IDE. 


Here is the link to my image that is pushed to Dockerhub:

https://hub.docker.com/repository/docker/muskansharmadocker/dockers/general


Also, Here are the commands that have been used:


Pull the Docker image

-> docker pull nginx:latest


Verify that the NGINX image was pulled successfully

-> docker images


Create the Dockerfile and Index.HTML


Build the image

-> docker build -t <new_image_name> .  #make sure to add a dot at the end


Verify that the image was built using command - docker images


Build and deploy the container

-> docker run -d --name <name-container> -p 8080:80 <new_image_name>


Check the newly created container 

-> docker ps -a


Verify that the container is running ( I was able to access the app in my localhost environment on port 8080 ) 	

-> http://localhost:8080/


Follow the below steps to push it to the Docker registry:


Login to Docker: docker login -u <docker username> 


Create a Repository in Docker


Commit the image :

-> docker commit <container id> <dockerhub username/docker hub repo name:tag name>


Push the Image to Dockerhub:

docker push dockerhub username/dockerhub repo:tagname


	
