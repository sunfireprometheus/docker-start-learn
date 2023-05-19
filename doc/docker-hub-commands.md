docker login -u <docker-user-name> // authentication to docker hub
docker tag <local-image-name>:<local-image-tag> <docker-user-name>/<docker-image-name>:<docker-tag> // recreate new image that same with docker hub image
docker push <docker-user-name>/<docker-image-name>:<docker-tag> // push