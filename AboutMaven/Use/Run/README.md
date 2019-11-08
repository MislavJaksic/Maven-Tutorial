## [Running Apache Maven](https://maven.apache.org/run.html)

### Common invocation

```
$: mvn package  # build project
$: mvn verify  # package and install locally

$: mvn clean deploy site-deploy  # life cycles can be chained

$: mvn archetype:generate  # invoke plugin goal
$: mvn checkstyle:check  # invoke plugin goal
```

### Life cycles

```
clean - pre-clean, clean, post-clean

default - validate, initialize, generate-sources, process-sources, generate-resources, process-resources, compile, process-classes, generate-test-sources, process-test-sources, generate-test-resources, process-test-resources, test-compile, process-test-classes, test, prepare-package, package, pre-integration-test, integration-test, post-integration-test, verify, install, deploy

site - pre-site, site, post-site, site-deploy
```
