# Create docker swarm service  - PHP Application
> sudo docker service create -p 80:80 --name php-service wahid74/phpcode

# Verify list docker swarm service
> sudo docker service ls

# list container for service
> sudo docker ps -a

--------------------------------------------------
# Create docker swarm service - Spring boot application
> sudo docker service create -p 8080:8081 --name ecom-service wahid74/ecom-webservice

# Verify list docker swarm service
> sudo docker service ls

# list container for service
> sudo docker ps -a