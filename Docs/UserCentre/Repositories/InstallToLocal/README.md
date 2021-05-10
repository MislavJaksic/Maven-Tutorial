## [Guide to installing 3rd party JARs](https://maven.apache.org/guides/mini/guide-3rd-party-jars-local.html)

There are JARs that don't exist in any public repository.  

`install-file` plugin in [Apache Maven Install Plugin](https://maven.apache.org/plugins/maven-install-plugin/) makes it easy to install such JARs.  

```
$: mvn install:install-file -Dfile=<path-to-file> -DgroupId=<group-id> -DartifactId=<artifact-id> -Dversion=<version> -Dpackaging=<packaging>  # install JAR without the POM file
$: mvn install:install-file -Dfile=<path-to-file> -DpomFile=<path-to-pomfile>  # install JAR if it has POM file
$: mvn org.apache.maven.plugins:maven-install-plugin:2.5.2:install-file -Dfile=<path-to-file>  # install JAR if it was built by maven
```
