# Host website within ubuntu image based container
> sudo docker run --name webserver -p 80:80 -it ubuntu /bin/bash

  > apt update
  > apt install apache2 -y 
  > service apache2 status
  > service apache2 start
  > service apache2 stop
  > apt install git -y
  > git clone https://github.com/wahidKhan74/circus-website.git
  > cp -r circus-website/* /var/www/html/
  