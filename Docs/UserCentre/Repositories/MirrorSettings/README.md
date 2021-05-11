## [Using Mirrors for Repositories](https://maven.apache.org/guides/mini/guide-mirror-settings.html)

Why use a `Mirror` rather then a `Repository`:
* Geographic vicinity
* Replace a `remote repository` with an `internal repository`
* Run a `repository manager` to provide a local cache to a mirror and need to use its URL instead

Using User Profile `${user.home}/.m2/settings.xml`:
```
<settings>
  ...
  <mirrors>
    <mirror>
      <id>other-mirror</id>
      <name>Other Mirror Repository</name>
      <url>https://other-mirror.repo.other-company.com/maven2</url>
      <mirrorOf>central</mirrorOf>
    </mirror>
  </mirrors>
  ...
</settings>
```

See [`settings.xml` description](../../../..Ref/MavenSettings).  

### Using A Single Repository

To Do

### Advanced Mirror Specification

A single mirror can handle multiple repositories which is typically used with a repository manager.  

ToDo

```
<settings>
  ...
  <mirrors>
    <mirror>
      <id>internal-repository</id>
      <name>Maven Repository Manager running on repo.mycompany.com</name>
      <url>http://repo.mycompany.com/proxy</url>
      <mirrorOf>external:*,!foo</mirrorOf>
    </mirror>
    <mirror>
      <id>foo-repository</id>
      <name>Foo</name>
      <url>http://repo.mycompany.com/foo</url>
      <mirrorOf>foo</mirrorOf>
    </mirror>
  </mirrors>
  ...
</settings>
```
