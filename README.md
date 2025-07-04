Flipkart Frontpage Clone with CI/CD Pipeline 

This project is a Flipkart front page UI clone built with HTML and CSS, integrated into a full CI/CD pipeline using Jenkins, deployed via Apache Tomcat, and the build artifact is stored in Nexus Artifactory.

1) Live Environment Setup

   All tools and services are hosted using IP and port in the browser:

   Service     -     URL Format	                   

   Jenkins     -     http://<ec2_instance ipaddress>:8080	       

   Tomcat      -     http://<ec2_instance ipaddress>:8080         

   Nexus Repo  -     http://<ec2_instance ipaddress>:8081	      

   Each service is hosted on its own EC2 instance or separate local/server environment, accessible via browser using the
   assigned IP address and port.

2) Tech Stack Used

   | Tool                 | Purpose                            |
   |--------------------- | ---------------------------------- |
   | HTML, CSS            | Frontend design                    |
   | Git & GitHub         | Version control and source hosting |
   | Apache Maven         | Build and package the project      |
   | Jenkins (on 8080)    | CI/CD pipeline automation          |
   | Nexus (on 8081)      | Artifactory to store WAR file      |
   | Apache Tomcat (8080) | Application deployment             |
   | EC2 or Localhost     | Hosting services                   |

3) Folder Structure

    satyajit_/
   
    ├── flipkart/
   
    │   ├── css/
   
    │   │   └── Image/
   
    │   └── html/
   
    │       └── index.html
   
    ├── pom.xml

5) Jenkins Pipeline Flow

   a) Clone Code: Jenkins pulls the latest source code from GitHub.

   b) Build: Maven compiles the project and packages it into a .war file.

   c) Artifactory Upload: The .war file is uploaded to Nexus Artifactory (http://<nexus-ip>:8081).

   d) Deploy: The .war file is copied or deployed to Tomcat (http://<tomcat-ip>:8080/satyajit_) — either manually or via shel

      script in Jenkins.


