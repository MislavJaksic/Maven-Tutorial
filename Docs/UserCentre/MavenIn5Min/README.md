## [Maven in 5 Minutes](https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html)

### Installation

[Instructions](../../../AboutMaven/Use/Install)

```
$: mvn -v
```

### Creating a Project

```
$: mvn archetype:generate  # ->
  # Choose a number or apply filter (format: [groupId:]artifactId): 1446:
  #   default
  # Choose org.apache.maven.archetypes:maven-archetype-quickstart version:
  #   8: 1.4
  # Define value for property 'groupId':
  #   mislavj
  # Define value for property 'artifactId':
  #   five-min
  # Define value for property 'version' 1.0-SNAPSHOT: :
  #   0.0.1
  # Define value for property 'package' mislavj: :
  #   default
```

#### The POM

The core of a project's configuration.  

#### Build the project

```
$: mvn package

$: java -cp target/five-min-0.0.1.jar mislavj.App
```

### Running Maven Tools

#### Maven Phases

Common default lifecycle phases:
1) validate: ensure correctness
2) compile: compile source
3) test: test compiled source
4) package: package compiled source
5) integration-test: run integration tests on a package
6) verify: validate package
7) install: install package into locally
8) deploy: copy package to a remote repository

Beyond default:
* clean: clean up artefacts
* site: generate docs
