# springboot-docker

This project tested on macbook using the list of following softwares.
 1. Docker - Mac
 2. Maven - 3.5
 3. Java 1.8
 4. Spring boot 1.5.7
 
 1. Check whether docker has been installed properly on machine or not.
   1.a: docker version
 1. Download project.
 2. Run
    >mvn install dockerfile:build
 3. Once build is done successfully, execute
    >docker images
    
   The above command will show list of images of Docker.
   
  REPOSITORY                   TAG                  IMAGE ID            CREATED             SIZE
  springio/springboot-docker    latest                7b7bdce792b7        44 minutes ago      116MB
  openjdk                       8-jdk-alpine         224765a6bdbe        3 months ago        102MB
  
 4. Now run 
   docker run -p 8086:8086 -t springio/springboot-docker
   
 5. Open browser and check whether your spring boot application is up and running or not.
 
    http://localhost:8086/docker/hello
    
 6. To stop the container
  > docker ps
  
  > docker stop <container id of springboot-docker>
    
 
