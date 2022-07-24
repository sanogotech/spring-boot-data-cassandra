# Spring Boot Cassandra CRUD example - Restful CRUD API

For more detail, please visit:
> [Spring Boot Cassandra CRUD example using Spring Data](https://bezkoder.com/spring-boot-cassandra-crud/)
>  https://www.datastax.com/blog/basic-rules-cassandra-data-modeling

##  Docs
DB Client Tools
- https://dbeaver.com/databases/

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
