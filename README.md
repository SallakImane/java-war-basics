# java-war-basics
How to compile, build and deploy JAVA EE war.

## Getting Started 

### `WAR` Definition 

File structure :

    + `jar` file contains : 

        > `META-INF/`       : this directory contains MANIFEST.MF
        > `*.class / *.jar` : All compiled classes and 3rt paty libraries

    + `war` file contains : 

        > `META-INF/`   : this directory contains MANIFEST.MF
        > `WEB-INF/`    : this directory contains
          > `web.xml`   : servlet definition
          > `classes/`  : compilet classes
          > `*.jar`     : 3rt party libraries

### Step 1 : Compile

1. Create a Java Servlet ”WEB-INF/com/imane/App.java” that extends `HttpServlet` and redefine doGet() methode.

2. Compile `App.java` to `App.class` with `servlet-api.jar` (Api that provide Servlet support) in the CLASSPATH:

        $ javac -cp servlet-api.jar WEB-INF/com/imane/App.java


### Step 2 : Build  
    $ jar cvf app.war WEB-INF
### Step 3 : Deploy

Copy the generated app.war to Tomcat Directory/webapps/

# Authors
 + **Sallak Imane** 