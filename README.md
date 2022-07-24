# Spring Boot Cassandra CRUD example - Restful CRUD API

For more detail, please visit:
>  https://bezkoder.com/spring-boot-cassandra-crud/ 

## Concepts

![Cassandra vs SQL ](https://github.com/sanogotech/spring-boot-data-cassandra/blob/master/docsCassandra/images/sqlvsCassandra.jpg)

##  Docs
DB Client Tools
- https://dbeaver.com/databases/
- https://stackoverflow.com/questions/28763294/sql-to-cassandra-data-model-structure
- https://www.datastax.com/blog/basic-rules-cassandra-data-
- https://www.youtube.com/watch?v=J-cSy5MeMOA

## Use Case
 * Apple  : 160 000 nodes/instances
 
```
- Ecommerce Search by
- Audit logs Search by
- Content Management search by

```

**(-- Application -- Queries/Use Cases  -- Data)   
- vs  ( Data -- Queries -- Application)

The main rule of Cassandra modeling is: start from your queries and denormalize. 

In your case, you would have 6 tables:
* employee_by_phone,
*  employee_by_location, 
*  employee_by_age and so on.

http://www.datastax.com/dev/blog/basic-rules-of-cassandra-data-modeling

However if you have a lot of multi-criteria queries like these, Cassandra (Datastax Enterprise edition) has SolR extension which will let you express richer queries. In this case your model may be right.

```
1) Select employee whose phone number = something;

2) Select employees who lives in 'XYZ' location;

3) Select employees whose age is > 40 years ;

4) Select employee whose Designation is a 'Manager' of Unit Name 'XYZ' ;

5) Select employees who work for over 1o hours a day;

6) Get names(not IDs) of all employees wh were working for client 'Apple';

```

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
