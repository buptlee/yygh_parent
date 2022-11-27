# yygh_parent

## About The Project
This is a sample project shows build microservices application with SpringBoot framework.

## How to run
### Prerequisite
Make sure you have the following components installed in your machine
1. JDK 1.8
2. Redis
3. RabbitMq
4. MySQL, download it from [here](https://dev.mysql.com/downloads/installer/)
5. MongoDB
6. Nacos 1.1.4, download it from [here](https://github.com/alibaba/nacos/releases/tag/1.1.4)
7. IntelliJ IDEA 2021.2.3 (Community Edition)
8. Docker, you can find detail steps in [here](https://docs.docker.com/desktop/install/windows-install/)
> You can install Redis, RabbitMq, MongoDB through Docker
### Install MongoDB, Redis, RabbitMq
1. Install MongoDB
   1. Open command window
   2. Run `docker pull mongo:latest`
   3. Run `docker run -d --restart=always -p 27017:27017 --name mymongo -v /data/db:/data/db -d mongo`
   4. Open Docker Desktop, you should be able to find mymongo in containers
   5. Open Terminal through Docker Desktop for `mymongo`
   6. Run `mongosh` goes into mongo db shell
   7. Run `show dbs` to see all existing databases
2. Install Redis
   1. Open command window
   2. Run `docker run --name my-redis -p 6379:6379 -d redis`
   3. Open Docker Desktop, you should be able to find my-redis in containers
   4. You can test redis through `redis-cli`, for more detail, you can find [here](https://redis.io/docs/manual/cli/#:~:text=The%20Redis%20command%20line%20interface%20(%20redis%2Dcli%20)%20is%20a,replies%20from%20the%20Redis%20server.)
3. Install RabbitMq
   1. Open command window
   2. Run `docker pull rabbitmq:management`
   3. Run `docker run -d -p 5672:5672 -p 15672:15672 --name rabbitmq rabbitmq:management`
   4. Open Docker Desktop, you should be able to find rabbitmq in containers, start the container
   5. Open browser and navigate to `http://localhost:15672/`
   6. If you can log in with `guest/guest`, the rabbitmq service is up
### Run Nacos
   1. Download nacos from [here](https://github.com/alibaba/nacos/releases/tag/1.1.4)
   2. Unzip the package and goes into bin folder
   3. Run `startup.cmd`
   4. Open browser and navigate to `http://localhost:8848/nacos`
   5. Login with `nacos/nacos`
   6. Once services get started, you should see all services in the service list
### Prepare Database
   1. Run sqls under sql folder in MySql Workbench
### Run Main Services 
   1. Open the project through intellij
   2. Install `Spring Initializr and Assistant`
   3. Restart the Intellij and you are good to go