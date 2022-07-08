// A Dockerfile is a text document which contains all the commands
// that a user can call on the command line to assemble an image.

# step 1: Create a docker file
> docker file is available in docker setup Dockerfile

# step 2: Docker build image
> sudo docker build -t phpcode -f Dockerfile/ filepath
> sudo docker build -t phpcode .

# step 3: Verify build images
> sudo docker images

# step 4: start/ run container from custom docker image
> sudo docker run --name phpserver -p 80:80 -d phpcode