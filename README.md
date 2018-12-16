![jcenter](https://img.shields.io/badge/_jcenter_-_8.191-6688ff.png?style=flat)
# alpn_boot
A java library for ALPN (used for HTTP2 negociation).

## Download ##

The maven artifacts are on [Bintray](https://bintray.com/programingjd/maven/info.jdavid.alpn/view)
and [jcenter](https://bintray.com/search?query=info.jdavid.alpn).

[Download](https://bintray.com/artifact/download/programingjd/maven/info/jdavid/alpn/8.191/alpn-boot-8.191.jar) the latest jar.

__Maven__

Include [those settings](https://bintray.com/repo/downloadMavenRepoSettingsFile/downloadSettings?repoPath=%2Fbintray%2Fjcenter)
 to be able to resolve jcenter artifacts.
```
<dependency>
  <groupId>info.jdavid.alpn</groupId>
  <artifactId>alpn-boot</artifactId>
  <version>8.191</version>
</dependency>
```
__Gradle__

Add jcenter to the list of maven repositories.
```
repositories {
  jcenter()
}
```
```
dependencies {
  compile 'info.jdavid.alpn:alpn-boot:8.191'
}
```

## Usage ##

You should use the version that matches your jdk version.


```
dependencies {
  compile "info.jdavid.alpn:alpn-boot:${getJDKVersion()}"
}

static def getJDKVersion() {
  def v = Runtime.class.getPackage().getImplementationVersion()
  return v.replaceFirst('1\\.([78])\\.0_([0-9]+)', '$1.$2')
}
```

```
java -Xbootclasspath/p:alpn-boot.jar ...
```