# HelloWorldJava

Simple HelloWorld Java application using Maven

[Maven Fundamentals](https://app.pluralsight.com/library/courses/maven-fundamentals/)

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
 - Add bin to Path env variable
 
 ## Maven
 
 Clean
 
 ```sh
 cd HelloWorldJava
 mvn clean
 ```
 
Compile
 
Maven Compiler Configuration
 
[Setting the -source and -target of the Java Compiler](https://maven.apache.org/plugins/maven-compiler-plugin/examples/set-compiler-source-and-target.html)

```xml
<project>
	<groupId>com.pluralsight</groupId>
	<artifactId>HelloWorld</artifactId>
	<version>1.0-SNAPSHOT</version>
	<modelVersion>4.0.0</modelVersion>
	<packaging>jar</packaging>

	<properties>
		<project.java.version>1.7</project.java.version>
		<project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
		<project.reporting.outputEncoding>UTF-8</project.reporting.outputEncoding>
	</properties>

	<build>
		<plugins>
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.8.1</version>
				<configuration>
					<source>${project.java.version}</source>
					<target>${project.java.version}</target>
					<encoding>${project.build.sourceEncoding}</encoding>
				</configuration>
			</plugin>
		</plugins>
	</build>
</project>
```

> Note: Merely setting the target option does not guarantee that your code actually runs on a JRE with the specified version. The pitfall is unintended usage of APIs that only exist in later JREs which would make your code fail at runtime with a linkage error. To avoid this issue, you can either configure the compiler's boot classpath to match the target JRE or use the Animal Sniffer Maven Plugin to verify your code doesn't use unintended APIs. In the same way, setting the source option does not guarantee that your code actually compiles on a JDK with the specified version. To compile your code with a specific JDK version, different than the one used to launch Maven, refer to the Compile Using A Different JDK example.

[Compiling Sources Using A Different JDK](https://maven.apache.org/plugins/maven-compiler-plugin/examples/compile-using-different-jdk.html)


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

### GitIgnore

- [Eclipse .gitignore](https://raw.githubusercontent.com/github/gitignore/master/Global/Eclipse.gitignore)

  Uncomment `.project` 
  
  > #&nbsp;Uncomment this line if you wish to ignore the project description file.
  >
  > #&nbsp;Typically, this file would be tracked if it contains build/dependency configurations:
  >
  > #&nbsp;.project
 
- [Maven .gitignore](https://raw.githubusercontent.com/github/gitignore/master/Maven.gitignore)

 
 
 
 
  