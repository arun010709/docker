# docker
Commands:
docker build -t <image-name> .
docker run -d -p 9090:8181 <image-name>
docker logs <container-id>
To go inside docker terminal:
docker exec -it <container-id> /bin/bash

Docker commit:
Create cloned image of an existing container using below command:
docker commit <original-container-id> <new-container-image-name>