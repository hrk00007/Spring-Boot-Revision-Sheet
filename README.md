# Spring-Boot-Revision-Sheet

## Introduction to Spring Boot
1. What is Spring Boot?
2. What is auto configuration?
3. What is starter (or) Autoconfiguration in Spring Boot? With Example?
4. What is Spring Boot-starter-files?
5. What is Starter Project?
6. What is the file Struture of Spring Boot/Starter Project?
7. What is Starter class OR Bootstrap class?
8. What is application.properties?
9. What is alternative of application.properties?
10. What are the build information files in Starter Project?Types of build information files?
11. What are the uses of build information files?
12. What inside of pom.xml(MAVEN)?
---
## Spring Configurations: 
1. In how many types we can configure Spring Boot classes?
2. What is Annotations based and Java based?Which one should be used?
### Annotations Based Configurations Questions
1. What is Annotations Based Configurations?
2. When should we Annonation based configuration?
3. What are the types of annotations?
4. What is Stereotype annotations?
   1. What is @Component?
   2. What is @Repository?
   3. What is @Service?
   4. What is @Controller?
   5. What is @RestController?
5. What is Data/Value Annotation?
   1. What is @Value?
   2. What is @ConfigurationProperties?
   3. What is @Order?
6. What is Link/Wire Annotations?
   1. What is @Autowired?
   2. What is @Qualifer?
   3. What is @Primary ?
### JAVA Based Configurations Questions
1. What is Java Based Configurations? 
2. What are the steps to write java based configuration?
3. Syntax of Java based configuration?
4. When should we java based configuration?

`**Conlusion Question:**` Which one is best annotations based or java based configuration?

---

## Spring Boot - Runners
1. What is A runner and why do we need it?
2. What are the types of Runners in Spring Boot?
3. What is the difference between Command Line and Application Runners?
4. Can we define multiple runners in one application?If yes , then want will be the order?
5. Can we define our own order of execution for Runners?
6. Which priority is higher in @Order annotations low value(1,-1,0) or high values(10 , 12 ,100)?
7. What will happen if the runner has no @Order?
---
## Component Scanning
1. What is a component scanning and what it does?
2. What is the base package in Component Scanning?
3. What is the default base package by Spring Boot?
4. Can we change basepackage by using @ComponentScan Annotations?If yes , then want how?
5. Can we provide multiple package name for Component Scanning?If yes then how?
6. Who will provide @ComponentScan in Spring Boot?
---   
## Properties Files
1. What is properties mean?
2. Does properties files are case sensitive?
3. What will happen if you repeat the same key with different values?
4. How properties files loaded in **Spring**?
5. How properties files loaded in **Spring Boot**?
6. What does classpath means in Spring/Spring Boot?
7. How to Read Data from .properties file?
### @Value annotations 
1. What is @Value Annotations and how it works?
2.  Answer the below Cases?
    - Case 1: same key with different values
    - Case 2: given key in @Value is not present
    - Case 3:  Wrong data type 
    - Case 4: Syntax Error in @Value in int and String
      - Syntax error with int
      - Syntax error with String
 ### @ConfigurationProperties annotations 
 1. What is @ConfigurationProperties Annotations and how it works?
2. What is prefix in @ConfigurationProperties?
3. What will happen if we don't have a prefix in @ConfigurationProperties?
4. Rules for defining key-val in @ConfigurationProperties? 
5. Working of @ConfigurationProperties?  
6. What is the difference between @Value and @ConfigurationProperties?
7. @ConfigurationProperties with
   -  Primitives
   -  List/Set/Array [1D collection]
   -  Map/Properties [2D Collection]
   -  Association Mapping (HAS-A with class)
####  Primitives  
1. What is the Syntax of primitives in application.properties with prefix?
2. How to Fetch those properties{key=val} into class primitive variables? 
3. Does configurationproperties uses Getter/Setter methods?
####  List/Set/Array [1D collection]
1. What is the Syntax of List/Set/Array  in application.properties with prefix?
2. What is the Shorthand of List/Set/Array in application.properties>
3. Who has more priority shortand or normal syntax?
####  Working with Map/Properties [2D Collection]
1. What is the Syntax of Map/Properties in application.properties with prefix?
   
### OTHER IMP QUESTION on properties files
1. Can we Load other properties file in Spring Boot?
2. If we rename application.properties to abcd.properties in Spring Boot then how to  provide that properties file manually?
3. Can we Load multiple external.properties files in spring Boot?    
4. If we have same key in multiple properties file then which one is taken by Spring boot?
5. What is the relation between @PropertySource and @Value, @ConfigurationProperties?
6. Can we Load .properties from external location[outside classpath]?
   -  Case 1 [Load .properties file from project location(outside src folder and inside project project folder)]
   -  Case 2 [Load .properties file from outside location(outside project folder or any hard disk location )]
7. How can we load a properties file from outside of classpath(src/main/resource) folder?
   - External Location: F Drive Or D Drive
   - Inside Folder Location: 
  
  ---
  ### Lombok API With Spring Boot
  1. What is Lombok API?Why we need it?
  2. What are the difference types of annotations provided by Lombok?
  3. How the code is generated using Annotations? 
  4. What is the role of @Getter,@Setter,@ToString and @EqualsAndHashCode?
  5. What is @NoArgsConstructor?
  6. What is @AllArgsConstructor?
  7. What is @RequiredArgsConstructor?
  8. What is the @NonNull annotation?
  9.  What is the difference between @NoArgsConstructor and @AllArgsConstructor and @RequiredArgsConstructor?

  #### Cases of Constructors Annotations 
  Convert these below written code into lombok generated code

  Case 1:
  ```java
@RequiredArgsConstructor
public class Product {
    private Integer pid;
    private String  pcode;
}
  ```

  Case 2:
```java
@NoArgsConstructor         
@RequiredArgsConstructor   
public class Product {
	@NonNull
    private Integer pid;
    private String  pcode;
}
  ```

  Case 3:
```java
@NoArgsConstructor        
@RequiredArgsConstructor   
@AllArgsConstructor        
public class Product {
	@NonNull
    private Integer pid;
    private String  pcode;
}  
```

  Case 4:
```java
@NoArgsConstructor         
@RequiredArgsConstructor   
public class Product {
	private Integer pid;
    private String  pcode;
}  
```
  Case 5:
```java
@AllArgsConstructor         
@NoArgsConstructor         
public class Product {
		
}  
```
  Case 6:
```java

@AllArgsConstructor        
 @NoArgsConstructor         
@RequiredArgsConstructor   
public class Product {
		
}
  
```
  Case 7:
```java
@AllArgsConstructor         
@RequiredArgsConstructor   
public class Product {
   private Integer pid;
}
  
```  
  Case 8:
```java
@NoArgsConstructor         
@RequiredArgsConstructor   

public class Product {
}  
```

10. What is @Data Annotations in Lombok?
 
 #### Cases of @Data Annotations   
case 1


 ```java
@Data
public class Product{
@NonNull
private Integer pid;
} 
 ```

 case 2
 ```java
 @Data
public class Product{
@NonNull
private Integer pid;
}
 ```
 case 3
 ```java
@Data
@NoArgsConstructor
public class Product{
@NonNull
private Integer pid;
}
 ```
 case 4
 ```java
@Data
@AllArgsConstructor
public class Product{
@NonNull
private Integer pid;
}
 ```
case 5
```java
@Data
@NoArgsConstructor
@RequiredArgsConstructor 
@AllArgsConstructor
public class Product{
@NonNull
private Integer pid;
private String code;
private Doubt amt;

}
``` 

11. How many constructor can be generated using Lombok?

---
### Yaml file
1. What is Yaml file or .yml file?
2. Why we need .yml file when we already have application.properties?
3. What is the syntax of .yml file?
4. What is SnakeYaml API?
5. How Yaml works internally in spring boot?
6. Convert below cases into application.properties into application.yml.

- Exercise 1
  
   ```java
   spring.ctx.code=NIT
   spring.ctx.type=ACTIVE
   spring.ds.model=ONE
   spring.ds.grade=A
   ```
- Exercise 2
  
   ```java
   my.app.subject[0]=ENG
   my.app.subject[1]=MATH
   my.app.subject[2]=SCI
   ```

- Exercise 3
  
   ```java
   code.model.status=ONE
   spring.ds.grade=A
   spring.ctx.service=TWO
   code.model.format=TEN
   spring.ctx.flte=active
   spring.ds.mode=none
   ```

#### YAML with [Primitive,1D & 2D collection,HAS-A(Assoication)]
7. Write the syntax and example for primitive variables in YAML?
8. Write the syntax and example for 1D collection(List/Set/Array) in YAML?
9. Write the syntax and example for 2D collection(Map/Properties) in YAML?
10. Write the syntax and example for  HAS-A (Association Mapping) in YAML?  
11. Write a code for implementing all above types?
---
### Command Line Arguments
1. What is command line arguments?
2. Write a syntax for code command line arguments in cmd?
3. How can we write main() method args using STS/ECLIPSE/INTELIJJ?
4. Does command line runner get's method argument or not?
5. Types of Command Line Arguments?
6. What is `Option arguments` and `Non-Option Arguments` and difference between them?
7. What is Option Arguments? What is the use of it?
8. What is Non-Option Arguments? What is the use of it?
9. Where are option arguments and non-Option Arguments stored?
---

### Spring Boot Profiles

1. What is Profile concepts and why do we need them?
2. What are two ways we can use profile concepts?
3. What is the syntax and Naming rule of the profiles using application.properties?
4. How to active profile at runtime?
5. What is Profiles Fallback in Spring Boot?
6. What is @Profile Annotations and what is the use of it?
7. What is the Problem with @Qualifer and why we need profile?
8. Write a sample code using @Profile annotations?
9. Write a sample code using @Profile with different application.properties?
10. How to use Profiles using YAML files?
11. What is Child Profile and why do we need it?
12. What is the Syntax of Child Profiles? 
   
---

### Spring Data JPA with Spring Boot
1. What are the types of databases?
2. Does Spring Data support operations in both of the databases?
3. Which Api we use for SQL type databases operations?
4. What is the difference between JDBC, JPA , Hibernate and ORM?
5. What is `dialect` and why do we need it?
6. Write the syntax of Oracle,MySQL dialect in application.properties?
7. What is `show-sql` property do?
8. What is `ddl-auto` property do? Explain the variou values for it?
9. What is the default value for `ddl-auto`?
10. What is Embedded Database? What is the use of it?
11. Give one example of Embedded Database?
12. Where is the data of Embedded Database stored?
13. What does @Entity annotation and where do we apply it?
14. What does @Id annotation and where do we apply it?
15. What does @Table annotation and where do we apply it?
16. What does @Column annotation and where do we apply it?
17. What is Repository in Spring Data JPA?
18. What are the different types of Repository? Explain the difference between them?
19. Which Design Pattern repositories classes uses internally?
20. What is CrudRepository? What is the syntax of CrudRepository?
21. Explain the CrudRepository interface important methods?
22. Write a code to connect to external db(oracle|MySQL|PostGres) using CrudRepository?
23. What is PagingAndSortingRepository? What is the syntax of PagingAndSortingRepository?
24. What is the difference between PagingAndSortingRepository and CrudRepository?
25. What are the additonal methods provided by PagingAndSortingRepository?
26. How to Sorting of Database based on column? Write a sample code for sorting the database output?
27. How to Sort database with Ascending and Descending order?
28. What is Pagination? Why do we need it?
29. How Pagination Works? OR What is the Pagination Process in data JPA?
30. Which method we use to provide Pagination?
31. What is Pageable and Page in PagingAndSortingRepository?
32. What is the method we can call with the Page object?   
33. Write a code for pagination using Pageable(Interface)?
34. Explain this line ```Pageable pageable= PageRequest.of(1,5);``` ?
35. What is JpaRepository? Why do we need it?
36. What is the difference between `JPARepository` and `PaginationAndSortingRepository`?
37. What additonal method we get from JPARepository?
38. Explain this JPA Annotations?
    - Data and Time Annotations: @Temporal and TemporalType 
    - LOB(LARGE OBJECT) Annotations:  @lob
39.  How to use @lob for image and large text file?
40. Write a code to implement @Temporal and @lob?
#### Custom Query Methods in JPA
1. What is Custom Query? Why do we need it?
2. What are the two ways of writing Custom Query?
3. What is findBy method in Customer Query? 
4. Write Syntax for findBy Method?
5. How to use findBy method for Vaiable Name?
6. Write findBy Syntax and Example for `SQL: select * from product where prod_vendor=?`   
7. How to use findBy method for Relational Operators?
8. Write findBy Syntax and Example for `SQL: select * from product where prod_cost>=?` 
9. How to use findBy method for IS Null/Not Null Operators?
10. Write findBy Syntax and Example for `SQL: select * from product where prod_grade is not null?`
11. Write a code to implement findBy for Variables,Relational and IS/NOT null operators?
12. How to use findBy method for like and not like operators?
13. Write findBy Syntax and Example for `SQL : select * from emp where ename like '?'` 
14. Write findBy Syntax and Example for `SQL : select * from emp where ename not like '?'` 
15. How to use findBy method for StartingWith/EndingWith/Containing Operator?
16. Write a code to implement findBy for `like, not like ,startingWith , endingWith and containing`?
17. How to use findBy method for `AND/OR` operators?
18. Write findBy Syntax and Example for `SQL : select * from emp where prod_name=? AND prod_cost>=?`
19. Write findBy Syntax and Example for `SQL : select * from emp where prod_name=? OR prod_cost>=?`
20. How to use findBy method for `Order By` operators?
21. Write findBy Syntax and Example for `SQL : select * from emp where prod_cost=? order by prod_vendor ASC;`
22. Write findBy Syntax and Example for `SQL : select * from emp where prod_cost=? order by prod_vendor DESC;`
23. Write a code to implement findBy for `AND/OR and OrderBy{ASC,DESC}`?
---
### Projections using findBy
1. What is Projections? Why do we need it?
2. What are the steps to write Projections?
3. Write down Syntax and Example of projections?
4. Write a code to implement projections?
---
### Custom Query using @Query Annotation