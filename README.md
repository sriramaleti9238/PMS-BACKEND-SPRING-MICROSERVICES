## PMS-SPRING-MICROSERVICES

PMS[Practice Management System] is a web-based application used as an interface for the patients to book their appointment based on the available physician timings. The booked appointments can be accepted or rejected by the physician and the approved appointments will be listed for the nurse to enter basic diagnosis and health information.
Once the nurse completed entering basic diagnosis information of the patient for the visit, it will be queued to the doctor to further enter the medication details during his consultation with the patients. Patients can access their health record at any time.

The application is developed on the basis of microservices architecture in the backend . The technologies used for each Microservice are, 
  - Spring Boot, 
  - Spring Cloud (Consul as a registry server), 
  - Spring Data,
  - Spring ORM, 
  - Spring AOP (Centralized logging and Centralized Exception Handling),
  - Spring JPA,
  - Jenkins (DevOps)
  - Docker (DevOps)
  - Prometheus (DevOps)
  - Grafana (DevOps)
  - JUnit (testing)
  - Mockito (testing)

To run the each microservice , 
1. first we need to run the Consul (registry service) 
2. If you want to perform the operations on localhost , you need to change the database settings in application-local.properties and the command to run the microservice is clean install spring-boot:run -Dspring.active.profiles=local
4. If you want to perform the operations on cloud , you need to change the database settings in application-production.properties and the command to run the microservice is clean install spring-boot:run -Dspring.active.profiles=production . Here i have used the rds database provided by AWS.
