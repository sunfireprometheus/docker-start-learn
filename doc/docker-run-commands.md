# ▲ Image
##  - build image
        docker build -t <image-name> . // in this case, the tag name will be latest.
        docker build -t <image-name>:<tag-name> .
        docker build --platform <platform-name> -t <image-name>:<tag-name> .
        *EX: docker build --platform linux/amd64 -t <image-name>:<tag-name> .
##  - list all images
        docker images

# ▲ Container
##  - build container
        docker run -dp <host-port>:<docker-internal-port> <image-name>:<tag-name> // run background
        docker run -p <host-port>:<docker-internal-port> <image-name>:<tag-name>  // run forground
        *EX: 
        docker run -dp 8000:3000 <image-name>:<tag-name>
        docker run -d ubuntu bash -c "shuf -i 1-10000 -n 1 -o /data.txt && tail -f /dev/null"
        docker run -dp 3000:3000 --mount type=volume,src=<volume-name>,target=/etc/todos <image-name>:<tag-name>
##  - stop container
        docker stop <container-id>
##  - remove container
        docker rm <container-id>
        docker rm -f <container-id> // stop and remove
##   - list all running docker containers
    docker ps

# ▲ Docker teminal
##  - run docker terminal
        docker exec <container-id> <commands>
        *EX: docker exec <container-id> cat /data.txt

# ▲ volume
##  - create volume
        docker volume create <volume-name>
##  - inspect voume
        docker volume inspect <volume-name>