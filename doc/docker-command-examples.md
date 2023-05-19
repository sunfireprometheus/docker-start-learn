# ▲ mysql
#   - docker network create todo-app
#   - docker run -d ` --network todo-app --network-alias mysql ` -v todo-mysql-data:/var/lib/mysql ` -e MYSQL_ROOT_PASSWORD=secret ` -e MYSQL_DATABASE=todos ` mysql:8.0
    - description
        1. connected todo-app network of docker
        2. created todo-mysql-data volume that is monuted at /var/lib/mysql
        3. set env(MYSQL_ROOT_PASSWORD=secret, MYSQL_DATABASE=todos)
        4. created mysql engine using mysql:8.0
#   - docker run -it --network todo-app nicolaka/netshoot
    - purpose // for monitoring, so it is not need for mysql engine & app