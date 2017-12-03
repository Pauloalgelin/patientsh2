Spring boot web application using Spring MVC, Hibernate JPA, Maven, Tomcat and H2.

Use it to maitain a list of Patients and their exams.

(1) Using Patients.war:
  - Download Patients.war
  (1.1) Using Tomcat
    - Place the file in your Tomcat/webapps
  (1.2) Using terminal
    - run "java -jar Patients.war"
  - visit the url: localhost:8081/Patients

(2) Run it from the source code:
  - Download /Patients
  - "cd Patients/"
  - "mvn spring-boot:run"
  - visit the url: localhost:8081/Patients
  
(3) Build the war from source:
  - Dowload /Patients
  - "cd Patients/"
  - "mvn package"
  - the war file will be created at Patients/target
  
Notes:
  - No guide for the application, because, hopefully, the GUI is good enough
  - Tomcat is running on port 8081.
    If you wish to change it, edit the file Patients/src/main/resources/application.properties (PROPERTIES)
    line "server.port=8081"
  - The default configuration is for H2 in memory database, if you want a non volatile memory,
    change the setting at PROPERTIES file. The first commented lines could work as a template for a MySQL database
  - The packaging must be war, because the views are JSP
    https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-developing-web-applications.html#boot-features-jsp-limitations
