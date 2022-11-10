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