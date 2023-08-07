
# docker-cmd cheat-sheet



#### Run a Jar as docker container.
1. Create a Dockerfile in project, add cmds (app.jar)
```bash
FROM eclipse-temurin:17-jdk-alpine
VOLUME /tmp
COPY target/*.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]
```
2. Run to create image locally 
```bash
docker build -t nkr4m/app:0.0.1 .
```
3. run a container out of the image
```bash
docker run --name <container-name> -d -p 8091:8091 nkr4m/app
```

#### To push the image to docker-hub.
1. login to docker hub
```bash
docker login
```
2. provide correct username/pass

3. docker push nkr4m/app

