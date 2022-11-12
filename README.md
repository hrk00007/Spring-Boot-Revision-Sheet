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
10.What are the build information files in Starter Project?Types of build information files?
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
  10. What is @Data Annotations in Lombok?
  #### Cases of Constructors Annotations 
  Case 1:

  Case 2:

  Case 3:

  Case 4:

  Case 5:

  Case 6:

  Case 7:
  
  Case 8:

---

