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
$: mvn surefire-report:report  # generate HTML report

# Note: see the XML test reports in `target/surefire-reports/TEST-**.xml`
# Note: see the HTML test reports in `target/site/surefire-report.html`
```

```
$: mvn package  # package compiled source

# Note: see the package in `target`
```

```
$: mvn install  # install to a local .m2 repository
```

```
$: mvn site  # generate a project website

# Note: see the HTML project report in `target/site/index.html`
```

### What is a SNAPSHOT version?

Used during the `release` phase to increment version.  

### How do I add resources to my JAR?

In the `resources` directory under `src`.  

### How do I filter resource files?

```
$: mvn process-resources "-Dcommand.line.prop=hello again"
# Note: changes `command.line.prop=${command.line.prop}` to `command.line.prop=hello again`
```

### How do I deploy my jar in my remote repository?

TODO

### How do I build other types of projects?
### How do I build more than one project at once?
