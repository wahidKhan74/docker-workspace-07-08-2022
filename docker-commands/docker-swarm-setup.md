# Create a manager node as e2 instance.
> 1. create ec2 instance
> 2. connect ec2 instance 
> 3. install docker

# Initialize a docker cluster ( manager node) 
> sudo docker swarm init   // Swarm initialized: current node (nn9srscjtominacj0jd8tckgx) is now a manager.

# Verify nodes in cluster 
> sudo docker node ls

# Create a worker node as ec2 instance.
> 1. create ec2 instance
> 2. connect ec2 instance 
> 3. install docker

# To add a worker to swarm manager , run the following command:
> sudo docker swarm join --token SWMTKN-1-3vl74kvqkda71c6hny8zs2e5fr65r3bjn5m0xgu24xaneudhi6-77mfiiot2nm2oziuypfypsyud 172.31.29.181:2377


# Create a worker node as ec2 instance.
> 1. create ec2 instance
> 2. connect ec2 instance 
> 3. install docker

# To add a worker to swarm manager , run the following command:
> sudo docker swarm join --token SWMTKN-1-3vl74kvqkda71c6hny8zs2e5fr65r3bjn5m0xgu24xaneudhi6-77mfiiot2nm2oziuypfypsyud 172.31.29.181:2377

# To add a manager to this swarm, run 
> sudo docker swarm join-token manager    // and follow the instructions.


# list docker swarm service 
> sudo docker service ls

# list  container for service
> sudo docker ps -a