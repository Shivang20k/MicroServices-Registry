After making Service Registry and doing service register in app.props of other microservices which will become client go to browser and check search this url "http://localhost:8761/"
Loading balancing is auto implemented in eureka server as If we run 2 instances of a service(make JAR of a service using "mvn clean package" and then run that jar from terminal using "java -jar CREATEDJARNAME.jar"  
Then change port of service whose jar is created and run that service from inttlj. Then we have 2 instance of same service.
