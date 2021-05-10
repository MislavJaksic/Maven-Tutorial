## [Maven](https://maven.apache.org/)

Maven is a Java build tool.  

```
Goal: action
Plugin: collection of goals
Build lifecycle: an ordered sequence of phases
Phase: a step in the build lifecycle; maps to goals
```

### Installation

IDEs such as Eclipse Java comes with Maven already preinstalled.  

```
# Note: install Java first
# Note: install Maven for your OS
$: mvn -v
```

```
$: scoop install maven  # for Windows
$: apt-get install maven  # for Linux
```

[Instructions](AboutMaven/Use/Install)

### Run

```
$: mvn [options] [<goal(s)>] [<phase(s)>]

$: mvn package  # build project
$: mvn verify  # package and install locally

$: mvn clean deploy site-deploy  # life cycles can be chained

$: mvn archetype:generate  # invoke plugin goal
$: mvn checkstyle:check  # invoke plugin goal
```

[Overview](AboutMaven/Use/Run)

### Configure

`settings.xml` in `USER_HOME/.m2` manages global Maven settings.  
`pom.xml` manages Maven project specific settings.  

[Overview](AboutMaven/Use/Configure)

### (Remote) Repository Management

`Repository manager`s manage repositories. They can be local, internal or remote.  



[Overview](Docs/UserCentre/Repositories)  

### Install 3rd Party JARs

`install-file` plugin in [Apache Maven Install Plugin](https://maven.apache.org/plugins/maven-install-plugin/) makes it easy to install such JARs.  

```
$: mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging>  # install JAR without the POM file
$: mvn install:install-file -Dfile=<path-to-file> -DpomFile=<path-to-pomfile>  # install JAR if it has POM file
$: mvn org.apache.maven.plugins:maven-install-plugin:2.5.2:install-file -Dfile=<path-to-file>  # install JAR if it was built by maven
```

[Install 3rd Party JAR](Docs/UserCentre/Repositories/InstallToLocal)  
