- build image
docker build -t <image-name> . // in this case, the tag name will be latest.
docker build -t <image-name>:<tag-name> .
docker build --platform <platform-name> -t <image-name>:<tag-name> .
*EX: docker build --platform linux/amd64 -t <image-name>:<tag-name> .

- build container
docker run -dp <host-port>:<docker-internal-port> <image-name>:<tag-name> // run background
docker run -p <host-port>:<docker-internal-port> <image-name>:<tag-name>  // run forground

*EX: docker run -dp 8000:3000 <image-name>:<tag-name>

- list all running docker containers
docker ps

- stop container
docker stop <container-id>

- remove container
docker rm <container-id>
docker rm -f <container-id> // stop and remove