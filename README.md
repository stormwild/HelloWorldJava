# HelloWorldJava

Simple HelloWorld Java application using Maven

 ## Pre-requisites
 
 - Java JDK (14)
 - Maven (3.6.3)
 
 ## Tools
 
 [Sprint Tool Suite 4](https://spring.io/tools)
 
 ### Setup
 
 - Run self extracting file
 - copy to desired installation directory C:\maven
 - Setup JAVA_HOME
 - Setup MAVEN_HOME
 
 ## Maven
 
 Clean
 
 ```sh
 cd HelloWorldJava
 mvn clean
 ```
 
Compile
 
 ```sh
 cd HelloWorldJava
 mvn compile
 cd target/classes
 java HelloWorld
 ```
 
Package
 
 ```sh
 cd HelloWorldJava
 mvn package
 cd target
 java -cp .\* HelloWorld
 ``` 
 
 
  