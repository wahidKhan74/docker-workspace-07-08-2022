# create / run a container
> sudo docker run -it ubuntu /bin/bash


# ssh / login a container
> sudo docker exec -it <container-name> /bin/bash
> sudo docker exec -it ubuntu /bin/bash

# start container
> sudo docker container start <container-name>/<container-id>
> sudo docker container start frosty_archimedes
> sudo docker container start 6ed12bc8667c

# stop container
> sudo docker container stop <container-name>/<container-id>
> sudo docker container stop frosty_archimedes
> sudo docker container stop 6ed12bc8667c

# restart container
> sudo docker container restart <container-name>/<container-id>
> sudo docker container restart frosty_archimedes
> sudo docker container restart 6ed12bc8667c

# delete container ( stop container can be deleted)
> sudo docker container rm <container-name>/<container-id>
> sudo docker container rm frosty_archimedes
> sudo docker container rm 6ed12bc8667c


# forcefull delete container ( delete a running container)
> sudo docker container rm -f <container-name>/<container-id>
> sudo docker container rm -f frosty_archimedes
> sudo docker container rm -f 6ed12bc8667c
