I found a great article at http://www.jroller.com/mrdon/entry/find_of_the_day_wagon that explained how to use Google code as a Maven repository.  Now, after I make updates, I can do:

```
mvn deploy
```

And it will handle uploading the new version to my svn repository here on Google code.

This is what allows you to add
```
  <repositories>
        <repository>
            <id>jstd-maven-plugin google code repo</id>
            <url>http://jstd-maven-plugin.googlecode.com/svn/maven2</url>
        </repository>
    </repositories>
```

to your POM and have automatic dependency resolution.

Thanks to kohsuke@dev.java.net for this!