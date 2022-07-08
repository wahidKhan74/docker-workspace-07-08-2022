Prerequisite : Java & Maven
> sudo apt install default-jdk -y
> sudo apt install maven -y


// A Dockerfile is a text document which contains all the commands
// that a user can call on the command line to assemble an image.

# step 1: Create a docker file
> docker file is available in docker setup Dockerfile

# step 2: Docker build image
> sudo docker build -t ecom-webservice -f Dockerfile/ filepath
> sudo docker build -t ecom-webservice .

# step 3: Verify build images
> sudo docker images

# step 4: start/ run container from custom docker image
> sudo docker run --name ecomserver -p 8080:8081 -d ecom-webservice