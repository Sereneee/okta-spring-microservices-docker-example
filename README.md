# Spring Microservices - Build Spring Microservices and Dockerize
1. Service Discovery
2. Config Server
3. Authentication: https://developer.okta.com/blog/2019/02/28/spring-microservices-docker
4. Additional link for microservices: https://developer.okta.com/blog/2019/05/22/java-microservices-spring-boot-spring-cloud

Send get request `http://localhost:8081` after running school-service application
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/03/31/8cda0743.png)


Send get request `http://localhost:8080` after running school-ui application
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/ecdd8.png)

Build and run the discovery server
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/3946af54.png)
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/8023a75e.png)

Configure both application school-service and school-ui to register with Eureka, then refresh the Eureka webpage and we'll see the 2 application there
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/d20b6b8d.png)

Add a configuration server, configure it, send request http://localhost:8888/school-ui.properties, see if it returns the correct configurations
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/e3762639.png)

Put school-ui behind an authorization layer (okta configuration - create a new Web Application in Okta’s dashboard) and Change School UI to Use Spring Cloud Config and OAuth 2.0

![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/d1296ed9.png)
![](https://devtraining2.blob.core.windows.net/devtraining2-images/2020/04/02/4e95dd22.png)

Use Docker to Package Spring Apps
*technology that allows creating system images similar to Virtual Machines but that shares the same Kernel of the host operating system. This feature increases system performance and startup time. Also, Docker provided an ingenious built system that guarantees once an image is created; it won’t be changed, ever. In other words: no more “it works on my machine!”








