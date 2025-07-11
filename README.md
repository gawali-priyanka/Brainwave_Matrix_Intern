Web Application Deployment

 AIM
To deploy and run a Java web application (loginwebapp.war) on Apache Tomcat, using Maven as the build and dependency management tool.
![image alt](https://github.com/gawali-priyanka/Brainwave_Matrix_Intern/blob/main/screenshots/Screenshot%202025-07-10%20170922.png?raw=true)
Tomcat Usage
Apache Tomcat is used as the servlet container to run the application.
Deploy the loginwebapp.war to Tomcat’s webapps directory.
Start and stop Tomcat using scripts:
$CATALINA_HOME/bin/startup.sh
$CATALINA_HOME/bin/shutdown.sh

Maven Usage
Used to compile, package the Java application into a .war file.
The WAR file is placed in the target/ directory after build:
command:mvn clean package

Edit .bash_profile
To configure Maven & Tomcat environment variables:
export MAVEN_HOME=/usr/local/apache-maven-3.9.6
export CATALINA_HOME=/usr/local/apache-tomcat-9.0.85
export PATH=$PATH:$MAVEN_HOME/bin:$CATALINA_HOME/bin
![image alt](https://raw.githubusercontent.com/gawali-priyanka/Brainwave_Matrix_Intern/8e72e8f051ecf0449561a85f68d4b5a54da46145/screenshots/Screenshot%202025-07-10%20165216.png)
 Deploy Application
 Step 1: Build the project
 mvn clean package
Step 2: Copy WAR to Tomcat
cp target/loginwebapp.war $CATALINA_HOME/webapps/
Step 3: Start Tomcat
![image alt](https://raw.githubusercontent.com/gawali-priyanka/Brainwave_Matrix_Intern/9df996be81b20fe894704f2c63e75b0b6c976fa2/screenshots/Screenshot%202025-07-10%20173355.png)
Access via URL
http://13.127.110.26:8080/loginwebapp
![image alt](https://raw.githubusercontent.com/gawali-priyanka/Brainwave_Matrix_Intern/a462f88bf74ae3a1e5220c288d7c546e25f0d51a/screenshots/Screenshot%202025-07-10%20170536.png)

Using Maven and Tomcat together, you automated the process to build and deploy your loginwebapp.war.
By editing .bash_profile, you made your environment reusable across sessions.
And finally, you accessed your application on the browser.


