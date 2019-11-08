## [Maven Getting Started Guide](https://maven.apache.org/guides/getting-started/index.html)

### Installation

[Instructions](../../../AboutMaven/Use/Install)

```
$: mvn -v
```

### What is Maven?

Maven applies patterns to a project's build infrastructure.  
Maven provides:
* builds
* documentation
* reporting
* dependencies
* SCMs
* releases
* distribution

### How do I make my first Maven project?

Use the Archetype plugin.  

[Instructions](../MavenIn5Min)

### Building, testing, packaging, and installing

```
$: mvn clean  # delete `target` directory
$: mvn compile  # compile source
```
```
$: mvn test  # run unit tests

# Note: see the XML test reports in `target/surefire-reports/TEST-**.xml`
```

```
$: mvn package  # package compiled source

# Note: see the package in `target`
```

```
$: mvn install  # install to a local repository
```

```
$: mvn site  # generate a website

# Note: see the XML test reports in `target/surefire-reports/TEST-**.xml`
```

### What is a SNAPSHOT version?

Used during the `release` phase to increment version.  

### How do I use plugins?
### How do I add resources to my JAR?
### How do I filter resource files?
### How do I use external dependencies?
### How do I deploy my jar in my remote repository?
### How do I create documentation?
### How do I build other types of projects?
### How do I build more than one project at once?

Archetype is a Maven plugin, a templating toolkit.  

"pom.xml" contents:  
```
<project xmlns="..."> -> top element
  <modelVersion>4.0.0</modelVersion> -> pom.xml version

  <groupId>mjaksic</groupId> -> author/organisation ID
  <artifactId>hello-world</artifactId> -> project ID

  <packaging>jar</packaging> -> how to package this project

  <version>1.0-SNAPSHOT</version> -> project version
  <name>Maven Quick Start Archetype</name> -> project name
  <url>http://maven.apache.org</url> -> project url

  <dependencies> -> project dependencies; enables "import"
    <dependency> -> sample dependency, JUnit 4
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.11</version>
      <scope>test</scope>
    </dependency>
  </dependencies>
</project>
```

To compile/test the project execute:  
```
:$ mvn compile -> compile
:$ mvn test -> compile and test
```

To package/install the project (for example construct a JAR) execute:  
```
:$ mvn package -> pack into JAR/WAR/...
:$ mvn install -> installs the JAR/WAR/...
```

You can add plugins and configure them in "pom.xml" like:  
```
...
<build>
  <plugins> -> plugins; they look like dependencies
    <plugin> -> sample plugin
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>3.3</version>
      <configuration> -> plugin configuration
        <source>1.5</source>
        <target>1.5</target>
      </configuration>
    </plugin>
  </plugins>
</build>
...
```

You can add resources to the project package (JAR/WAR/...) such as properties.  
Place the properties/settings in:  
```
".../resources/META-INF/_settings_file_name.properties"
```

Build time values can be filtered/referenced from inside the resource file/"pom.xml":
```
<build>
  <resources>
    <resource>
      <directory>src/main/resources</directory>
      <filtering>true</filtering>
    </resource>
  </resources>
</build>
```
```
<properties>
  <_property_name>_property_value</_property_name>
</properties>
```

External dependencies must have at least four elements:  
```
...
<dependency>
  <groupId>mjaksic</groupId>
  <artifactId>hello-world</artifactId>
  <version>0.1</version>
  <scope>compile/test/runtime</scope>
</dependency>
...
```
You can search Maven Repositories for external dependencies.  

Deploy package (JAR/WAR/...) to a remote/private repository.  
TODO  

Generate documentation.  
TODO  
