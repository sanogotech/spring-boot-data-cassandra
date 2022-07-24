# Spring Boot Cassandra CRUD example - Restful CRUD API

For more detail, please visit:
>  https://bezkoder.com/spring-boot-cassandra-crud/ 


##  Docs
DB Client Tools
- https://dbeaver.com/databases/
- https://www.datastax.com/blog/basic-rules-cassandra-data-modeling

## Configuration 

```
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-starter-data-cassandra</artifactId>
</dependency>

 ```
 * application.proproties
 ```
spring.data.cassandra.keyspace-name=bezkoder
spring.data.cassandra.contact-points=127.0.0.1
spring.data.cassandra.port=9042
```
## Run Spring Boot application
```
mvn spring-boot:run
```
