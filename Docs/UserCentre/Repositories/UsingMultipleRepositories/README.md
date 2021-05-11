## [Setting up Multiple Repositories](https://maven.apache.org/guides/mini/guide-multiple-repositories.html)

Using `pom.xml`:
```
<project>
...
  <repositories>
    <repository>
      <id>my-repo1</id>
      <name>your custom repo</name>
      <url>http://jarsm2.dyndns.dk</url>
    </repository>
    <repository>
      <id>my-repo2</id>
      <name>your custom repo</name>
      <url>http://jarsm2.dyndns.dk</url>
    </repository>
  </repositories>
...
</project>
```

Using `path/to/Maven-Home/conf/settings.xml` or `${user.home}/.m2/settings.xml`:
```
<settings>
 ...
 <profiles>
   ...
   <profile>
     <id>myprofile</id>
     <repositories>
       <repository>
    *  <id>my-repo2</id>
    *  <name>your custom repo</name>
    *  <url>http://jarsm2.dyndns.dk</url>
       </repository>
     </repositories>
   </profile>
   ...
 </profiles>

 <activeProfiles>
   <activeProfile>myprofile</activeProfile>
 </activeProfiles>
 ...
</settings>
```

If using the User Profile specific `${user.home}/.m2/settings.xml`, don't forget to select that Profile:
```
$: mvn -Pmyprofile ...
```

### Repository Order

Query order:
1) effective settings:
    * Global `settings.xml`
    * User `settings.xml`
2) local effective build POM:
    * Local `pom.xml`
    * Parent POMs, recursively
    * Super POM
3) effective POMs from dependency path to the artifact.

Review them with:
```
$: mvn help:effective-settings
$: mvn help:effective-pom -Dverbose
```
