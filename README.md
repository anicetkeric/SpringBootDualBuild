# SpringBootDualBuild
Dual jar/war build for Spring Boot using Profiles

The names of the configurations files should match with the pattern application-{custom_suffix}.properties. create more property files and add the "profile" name as the suffix.

Create application.properties files:

  - application-dev.properties 
  - application-prod.properties

```xml
 modify pom.xml
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
    <id>release</id>
    <properties>
        <activatedProperties>release</activatedProperties>
    </properties>
</profile>


```
