# admin-server

## Uses of admin project
The admin project monitors logs, REST end point usage, health status of applications and much more of connected spring boot microservices. To connect a microservice to the admin, you need to add the following into the spring boot microservice application.properties:
```
spring.boot.admin.client.url=http://admin:8080
spring.boot.admin.client.instance.prefer-ip=true
```
There are a few other useful settings you can add, but these aren't relevant for initial set up.

## How to build
This is built via maven. In the pom file, you'll see some docker set up. If you run 'mvn clean install -Ddocker', maven will build you a docker image and tag it as latest and with whatever the version of the pom is.

## How to run
This is just like an other spring boot project. It can be run via the main method on a tomcat server. However, if you checkout the docker project, you can run this admin project with  docker-compose.
