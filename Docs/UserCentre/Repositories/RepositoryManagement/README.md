## [Best Practice - Using a Repository Manager](https://maven.apache.org/repository-management.html)

A `repository manager` is a dedicated server application designed to manage repositories of binary components.

### Purpose

* Act as dedicated [proxy server for public Maven repositories](../MirrorSettings)
* Provide repositories as a deployment destination for your Maven project outputs

### Benefits and Features

Benefits and features:
* significantly reduced number of downloads off remote repositories, saving time and bandwidth resulting in increased build performance
* improved build stability due to reduced reliance on external repositories
* increased performance for interaction with remote SNAPSHOT repositories
* potential for control of consumed and provided artifacts
* creates a central storage and access to artifacts and meta data about them exposing build outputs to consumer such as other projects and developers, but also QA or operations teams or even customers
* provides an effective platform for exchanging binary artifacts within your organization and beyond without the need for building artifact from source

### Available Repository Managers

The following list (alphabetical order) of open source and commercial repository managers are known to support the repository format used by Maven. Please refer to the respective linked web sites for further information about repository management in general and the features provided by these products.

Open source:
* Apache Archiva
* JFrog Artifactory Open Source
* Sonatype Nexus OSS
* Reposilite

Commercial:
* CloudRepo
* Cloudsmith Package
* Dist
* JFrog Artifactory Pro
* MyGet
* Sonatype Nexus Pro
* packagecloud.io
