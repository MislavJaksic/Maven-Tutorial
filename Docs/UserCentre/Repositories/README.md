## [Introduction to Repositories](https://maven.apache.org/guides/introduction/introduction-to-repositories.html)

### Artifact Repositories

A repository in holds build artifacts and dependencies.  

Repositories:
* local - a directory on the computer. It caches remote downloads and contains temporary build artifacts that you have not yet released.
* remote - might be a truly remote or internal repositories. Used to share private artifacts between development teams and for releases.

### Using Repositories

Local ones only need to be occasionally cleaned if you are low on disk space.  

Remote ones are downloading and uploading.  

#### Downloading from a Remote Repository

By default, Maven will download from the central repository:
```
https://repo.maven.apache.org/maven2/
```

Use [mirrors](../MirrorSettings) to download from another repository.  

Set mirrors in:
* `settings.xml`
* [`pom.xml`](../UsingMultipleRepositories)

### Building Offline

To build offline and prevent plugins from accessing the Internet use:
```
$: mvn -o package
```
```
### Uploading to a Remote Repository

While this is possible for any type of remote repository, you must have the permission to do so. To have someone upload to the Central Maven repository, see Repository Center.
### Internal Repositories

When using Maven, particularly in a corporate environment, connecting to the internet to download dependencies is not acceptable for security, speed or bandwidth reasons. For that reason, it is desirable to set up an internal repository to house a copy of artifacts, and to publish private artifacts to.

Such an internal repository can be downloaded using HTTP or the file system (with a file:// URL), and uploaded to using SCP, FTP, or a file copy.

As far as Maven is concerned, there is nothing special about this repository: it is another remote repository that contains artifacts to download to a user's local cache, and is a publish destination for artifact releases.

Additionally, you may want to share the repository server with your generated project sites. For more information on creating and deploying sites, see Creating a Site.
### Setting up the Internal Repository

To set up an internal repository just requires that you have a place to put it, and then copy required artifacts there using the same layout as in a remote repository such as repo.maven.apache.org.

It is not recommended that you scrape or rsync:// a full copy of central as there is a large amount of data there and doing so will get you banned. You can use a program such as those described on the Repository Management page to run your internal repository's server, download from the internet as required, and then hold the artifacts in your internal repository for faster downloading later.

The other options available are to manually download and vet releases, then copy them to the internal repository, or to have Maven download them for a user, and manually upload the vetted artifacts to the internal repository which is used for releases. This step is the only one available for artifacts where the license forbids their distribution automatically, such as several J2EE JARs provided by Sun. Refer to the Guide to coping with SUN JARs document for more information.

It should be noted that Maven intends to include enhanced support for such features in the future, including click through licenses on downloading, and verification of signatures.
### Using the Internal Repository

Using the internal repository is quite simple. Simply make a change to add a repositories element:

    <project>
      ...
      <repositories>
        <repository>
          <id>my-internal-site</id>
          <url>http://myserver/repo</url>
        </repository>
      </repositories>
      ...
    </project>

If your internal repository requires authentication, the id element can be used in your settings file to specify login information.
### Deploying to the Internal Repository

One of the most important reasons to have one or more internal repositories is to be able to publish your own private releases.

To publish to the repository, you will need to have access via one of SCP, SFTP, FTP, WebDAV, or the filesystem. Connectivity is accomplished with the various wagons. Some wagons may need to be added as extension to your build.
```
