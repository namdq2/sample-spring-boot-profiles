# Spring Boot Profiles for DEV and PROD Environments
## Define the profiles
We can easily define the profiles by adding the following XML to the project's pom.xml file:
><profiles>
         <profile>
             <id>dev</id>
             <properties>
                 <activatedProperties>dev</activatedProperties>
             </properties>
             <activation>
                 <activeByDefault>true</activeByDefault>
             </activation>
         </profile>
         <profile>
             <id>prod</id>
             <properties>
                 <activatedProperties>prod</activatedProperties>
             </properties>
         </profile>
     </profiles>
>
## Create the two new environment-specific property files
- application-dev.properties
- application-prod.properties

## Specifying the Profile at Build Time
> mvn -Pprod clean install

>java –jar -Dspring.profiles.active=prod app.jar