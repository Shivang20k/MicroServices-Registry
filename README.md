1. After making a Service Registry and doing the service register in the app.props of other microservices that will become clients go to the browser and search this URL "http://localhost:8761/"
2. Loading balancing is auto-implemented in the eureka server as If we run 2 instances of a service(make JAR of a service using "mvn clean package" and then run that jar from terminal using "java -jar CREATEDJARNAME.jar"
3. But to enable this auto-load balancer add this dependency in eureka-client(other microservice's pom.xml)
    <dependency>
			<groupId>org.springframework.cloud</groupId>
			<artifactId>spring-cloud-starter-loadbalancer</artifactId>
		</dependency>
5. Then change the port of the service whose jar is created and run that service from inttlj. Then we have 2 instances of the same service.
6. Since we have  registered the other microservices with their names. So instead of hard coding the URL of microservices in feign client use their name eg.) @FeignClient(name = "PASSENGER-SERVICE")
