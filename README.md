# HelloWorldJava

Simple HelloWorld Java application using Maven

 ## Pre-requisites
 
 - Java JDK (14)
 - Maven (3.6.3)
 
 ## Tools
 
 [Spring Tools 4 for Eclipse](https://spring.io/tools)
 
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
 
## Notes
 
### UTF-8 Encoding
 
Configure UTF-8 encoding for all content types in Eclipse (Spring Tools 4): 

[How to support UTF-8 encoding in Eclipse](https://stackoverflow.com/questions/9180981/how-to-support-utf-8-encoding-in-eclipse)
 
### Configure UTF-8 encoding in maven
 
[How to configure encoding in Maven?](https://stackoverflow.com/questions/3017695/how-to-configure-encoding-in-maven)
 
### Maven Compiler Configuration
 
[Setting the -source and -target of the Java Compiler](https://maven.apache.org/plugins/maven-compiler-plugin/examples/set-compiler-source-and-target.html)
  
### Properties

[Properties](https://maven.apache.org/pom.html#Properties)


 
 
 
 
  