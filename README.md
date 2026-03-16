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

Creating images without Dockerfile:
Google JIB:
Add google jib plugin in pom.xml under <plugin> section - jib-maven-plugin
Also need a configuration tag under plugin section to define the docker image name-> <configuration><to>spring-docker:4.0</to></configuration>
mvn compile jib:dockerBuild 

Spring starter pack(From Spring boot 2.3.x version):
mvn spring-boot:build-image
mvn spring-boot:build-image -Dspring-boot.build-image.imageName=spring-docker-app:v2

Docker Hub:
Registry of docker images.


1.Create account in docker hub.
2.Create a tag for your image with your username.
docker tag <image-name> <tagged-image-name>
3.Push the image.	
docker push <tagged-image-name>
4.To use image, user can pull:
docker pull <tagged-image-name>
	