# Jenkins is java based CI server :: 
> create a ec2 instance
> install java and maven
> install jenkins server
> install docker 

# Install java and maven
> sudo apt install default-jdk -y
> sudo apt install maven -y
> sudo java -version
> sudo mvn -v

# Install Jenkins server in ubuntu 22.0.4

> curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null

> echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

> sudo apt-get update
> sudo apt-get install jenkins -y 

# Service verification
> sudo service jenkins status
> sudo service jenkins start
> sudo service jenkins stop
> sudo service jenkins restart 