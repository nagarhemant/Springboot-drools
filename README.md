# Springboot-drools
Drools is an opensource brms engine
Drools is a Business Rule Management System (BRMS) solution. It provides a rule engine which processes facts and produces output as a result of rules and facts processing. Centralization of business logic makes it possible to introduce changes fast and cheap.

### Drools Basics
We are going to look at basic concepts of Drools:
- Facts – represents data that serves as input for rules
- Working Memory – a storage with Facts, where they are used for pattern matching and can be modified, inserted and removed
- Rule – represents a single rule which associates Facts with matching actions. It can be written in Drools Rule Language in the .drl files or as Decision Table in an excel spreadsheet
- Knowledge Session – it holds all the resources required for firing rules; all Facts are inserted into session, and then matching rules are fired
- Knowledge Base – represents the knowledge in the Drools ecosystem, it has the information about the resources where Rules are found, and also it creates the Knowledge Session
- Module – A module holds multiple Knowledge Bases which can hold different sessions
### Springboot configuration
#### POM file
 
 ```xml
<dependency>
<groupId>org.drools</groupId>
<artifactId>drools-core</artifactId>
<version>6.4.0.Final</version>
</dependency><!-- https://mvnrepository.com/artifact/org.drools/drools-compiler -->
<dependency>
<groupId>org.drools</groupId>
<artifactId>drools-compiler</artifactId>
<version>6.4.0.Final</version>
</dependency><!-- https://mvnrepository.com/artifact/org.kie/kie-api -->
<dependency>
<groupId>org.kie</groupId>
<artifactId>kie-api</artifactId>
<version>6.4.0.Final</version>
</dependency>
 ```
 #### rule file
 - create a folder inside src/main/resources
 - create a file that has .drl extension
 #### ksession
 - create a folder named `META-INF`
 