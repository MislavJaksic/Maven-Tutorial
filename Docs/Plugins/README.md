## [Available Plugins](https://maven.apache.org/plugins/index.html)

Plugin types:
* build: executed during the build and configured in `<build/>` in `pom.xml`
* reporting: executed during the site generation and configured in `<reporting/>` in `pom.xml`

### Supported By The Maven Project

| Core plugins            | Description                                                                  |
|-------------------------|------------------------------------------------------------------------------|
|  clean                  | Clean up after the build.                                                    |
|  compiler               | Compiles Java sources.                                                       |
|  deploy                 | Deploy the built artefact to the remote repository.                          |
|  failsafe               | Run the JUnit integration tests in an isolated classloader.                  |
|  install                | Install the built artefact into the local repository.                        |
|  resources              | Copy the resources to the output directory for including in the JAR.         |
|  site                   | Generate a site for the current project.                                     |
|  surefire               | Run the JUnit unit tests in an isolated classloader.                         |
|  verifier               | Useful for integration tests - verifies the existence of certain conditions. |

| Packaging types/tools   | Description                                                         |
|-------------------------|---------------------------------------------------------------------|
|  ear                    | Generate an EAR from the current project.                           |
|  ejb                    | Build an EJB (and optional client) from the current project.        |
|  jar                    | Build a JAR from the current project.                               |
|  rar                    | Build a RAR from the current project.                               |
|  war                    | Build a WAR from the current project.                               |
|  app-client/acr         | Build a JavaEE application client from the current project.         |
|  shade                  | Build an Uber-JAR from the current project, including dependencies. |
|  source                 | Build a source-JAR from the current project.                        |
|  jlink                  | Build Java Run Time Image.                                          |
|  jmod                   | Build Java JMod files.                                              |

| Reporting plugins       | Description                                                   |
|-------------------------|---------------------------------------------------------------|
|  changelog              | Generate a list of recent changes from your SCM.              |
|  changes                | Generate a report from an issue tracker or a change document. |
|  checkstyle             | Generate a Checkstyle report.                                 |
|  doap                   | Generate a Description of a Project (DOAP) file from a POM.   |
|  docck                  | Documentation checker plugin.                                 |
|  javadoc                | Generate Javadoc for the project.                             |
|  jdeps                  | Run JDK's JDeps tool on the project.                          |
|  jxr                    | Generate a source cross reference.                            |
|  linkcheck              | Generate a Linkcheck report of your project's documentation.  |
|  pmd                    | Generate a PMD report.                                        |
|  project-info-reports   | Generate standard project reports.                            |
|  surefire-report        | Generate a report based on the results of unit tests.         |

| Tools                   | Description                                                                                     |
|-------------------------|-------------------------------------------------------------------------------------------------|
|  antrun                 | Run a set of ant tasks from a phase of the build.                                               |
|  archetype              | Generate a skeleton project structure from an archetype.                                        |
|  assembly               | Build an assembly (distribution) of sources and/or binaries.                                    |
|  dependency             | Dependency manipulation (copy, unpack) and analysis.                                            |
|  enforcer               | Environmental constraint checking (Maven Version, JDK etc), User Custom Rule Execution.         |
|  gpg                    | Create signatures for the artefacts and poms.                                                   |
|  help                   | Get information about the working environment for the project.                                  |
|  invoker                | Run a set of Maven projects and verify the output.                                              |
|  jarsigner              | Signs or verifies project artefacts.                                                            |
|  jdeprscan              | Run JDK's JDeprScan tool on the project.                                                        |
|  patch                  | Use the gnu patch tool to apply patch files to source code.                                     |
|  pdf                    | Generate a PDF version of your project's documentation.                                         |
|  plugin                 | Create a Maven plugin descriptor for any mojos found in the source tree, to include in the JAR. |
|  release                | Release the current project - updating the POM and tagging in the SCM.                          |
|  remote-resources       | Copy remote resources to the output directory for inclusion in the artefact.                    |
|  scm                    | Execute SCM commands for the current project.                                                   |
|  scm-publish            | Publish your Maven website to a scm location.                                                   |
|  stage                  | Assists with release staging and promotion.                                                     |
|  toolchains             | Allows to share configuration across plugins.                                                   |

### Outside The Maven Land

#### At MojoHaus (formerly codehaus.org)

| Plugin            | Description                                                                      |
|-------------------|----------------------------------------------------------------------------------|
|  animal-sniffer   | Build signatures of APIs (JDK for example) and checks your classes against them. |
|  build-helper     | Attach extra artifacts and source folders to build.                              |
|  castor           | Generate sources from an XSD using Castor.                                       |
|  clirr            | Compare binaries or sources for compatibility using Clirr                        |
|  javacc           | Generate sources from a JavaCC grammar.                                          |
|  jdepend          | Generate a report on code metrics using JDepend.                                 |
|  nar-maven-plugin | Compiles C, C++, Fortran for different architectures.                            |
|  native           | Compiles C and C++ code with native compilers.                                   |
|  sql              | Executes SQL scripts from files or inline.                                       |
|  taglist          | Generate a list of tasks based on tags in your code.                             |
|  versions         | Manage versions of your project, its modules, dependencies and plugins.          |

#### Misc

| Plugin                  | Description                                                                        |
|-------------------------|------------------------------------------------------------------------------------|
|  cargo                  | Start/stop/configure J2EE containers and deploy to them.                           |
|  clover                 | Generate a Clover report.                                                          |
|  jetty                  | Jetty Run a Jetty container for rapid webapp development.                          |
|  jalopy                 | Use Jalopy to format your source code.                                             |
|  rat                    | Release Audit Tool (RAT) to verify files.                                          |
|  Genesis Plugins        | Verify legal files in artifacts.                                                   |
|  Apache Tomcat          | Run an Apache Tomcat container for rapid webapp development.                       |
|  OWASP dependency-check | Run OWASP Dependency-Check. Identifies known, publicly disclosed, vulnerabilities. |
