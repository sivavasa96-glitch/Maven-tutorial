Maveen:

Maven install in windows:
==========================
1. First you install the java file jdk below link:

Download JDK 8 / 11 / 17 (recommended: JDK 17) from:

Oracle JDK or

https://download.oracle.com/java/25/latest/jdk-25_windows-x64_bin.exe (sha256)

2. once download thw jdk file then install in your system


3. once install is done verify the in your system
check the path for windows C:\Program Files\Java

Verify Java installation:

java -version

maveen install in your system:
============================

1. Go to the Apache Maven official site download the latest version for the support windows version
https://maven.apache.org/download.cgi

2. Download Binary zip archive (e.g., apache-maven-3.9.x-bin.zip)

3. Extract it to: C:\Program Files\Apache\Maven

Set Environment Variables:
=============================
Open System Properties → Environment Variables

Under System Variables → New

Variable name: MAVEN_HOME
Variable value: C:\Program Files\Apache\Maven

Update PATH:
============

Edit Path (System Variables)

Add: C:\Program Files\Apache\Maven/bin

Verify JAVA_HOME:
===================
Set Environment Variables:
=============================
Open System Properties → Environment Variables

Under System Variables → New for apache

Variable name: MAVEN_HOME
Variable value: C:\Users\ADMIN\Downloads\apache-maven-3.9.11-bin\apache-maven-3.9.11

edit path

%MAVEN_HOME%\bin

Then click on ok
check the mvn version
mvn -version





Make sure it is set:

JAVA_HOME = C:\Program Files\Java\jdk-17

create the mvn project for the windows:
=======================================
go to the cmd prompt
1. mvn archetype:generate

Choose a number or apply filter (format: [groupId:]artifactId, case sensitive co
ntains): 2309: " its showing avalibility plugins enter it"
Choose org.apache.maven.archetypes:maven-archetype-quickstart version:

Choose a number: 9:
[INFO] Using property: javaCompilerVersion = 17
[INFO] Using property: junitVersion = 5.11.0
Define value for property 'groupId': com.onlineselenium
Define value for property 'artifactId': mymavenproject
Define value for property 'version' 1.0-SNAPSHOT:
Define value for property 'package' com.onlineselenium:
Confirm properties configuration:
javaCompilerVersion: 17
junitVersion: 5.11.0
groupId: com.onlineselenium
artifactId: mymavenproject
version: 1.0-SNAPSHOT
package: com.onlineselenium
 Y: y
 
 2. once bullid is sucess
 
 3. 

 POM:
 ====
 POM stands for Project Object Model. The pom.xml file is an XML file that serves as the fundamental configuration file for a Maven project. It contains all the necessary information and configuration details Maven uses to build, test, and deploy the project. 
 
 Key information specified in a pom.xml file includes:
1.roject metadata: The project's unique identifiers (groupId, artifactId, version), name, description, and URL.
2.Dependencies: External libraries (JAR files) that the project requires. Maven automatically downloads these from repositories.
3.Plugins: Tools used to perform specific build tasks, such as compiling source code, running tests, or generating documentation.
4.Build profiles: Environment-specific configurations for development, testing, or production.
5.Source and output directories: The locations of source code, test code, and where the build artifacts should be placed. 

mvn compile:
in pom.xml whatever have you updated in xml . its download in localserver

Maven Build Lifecycle (Basic)
validate → compile → test → package → verify → install → deploy

1.validate: Checks that the project is correct and all necessary information is available.
2.compile: Compiles the source code of the project.
3.test: Runs tests against the compiled source code using a suitable unit testing framework (like JUnit or TestNG).
4.package: Takes the compiled code and packages it in its distributable format, such as a JAR or WAR file.
5.verify: Runs checks on the results of integration tests to ensure quality criteria are met.
6.install: Installs the package into the local repository for use as a dependency in other locally built projects.
7.deploy: Copies the final package to the remote repository for sharing with other developers and projects. 

commands:
========

338  mvn eclipse:eclipse

  352  cd mymavenproject/
  353  ls
  354  mvn compile : mvn compile is a Maven command used to compile the source code of a Java project
  355  mvn test
  356  mvn package
  357  mvn install
  358  mvn eclipse:eclipse
  359  mvn compile
  360  mvn compile
  361  mvn package

How to create the web application using maven in eclipse:
=========================================================

1. first down load the eclipse software

https://www.eclipse.org/downloads/

2. once install is done then open the eclipse sotware

3. now we will create the web apllication using Maven
	a. open the eclipse software
	b. click the new button and selected maven project option
    c. whatever we have selected particals location you choice the location and click the next button
	d. the filter the maven and selected maven webapp option click the next 
	f. we shoulb be mention the groupid(com.sivakumar) and artifact id(project name) and click finish 
4. now its created the web application in eclipse 
5. we need the java software also so we can download the java
	a. go to my project and rightclick choice the propertices
	b. its opened propertices go to libraies and selecte the java bulid path and selected java
	c. now we can selected the edit option
	d. what ever have you install the java software in local mechine its showing java vesrion
	f. now we can selected the java and click the apply
	
	
how to build and deploy the web application:
==============================================
Already we have created the maven project open the same project the eclipse
1. right click the your project run the maven install
2. once build is sucess its created the target folder in your Project
3. its should be create the war file or jar file its Dependencies on your Project
4. Right click on your project ist showing RUN AS option and choice the tomcat server
5. once build is sucess its showing webpage

	
	
