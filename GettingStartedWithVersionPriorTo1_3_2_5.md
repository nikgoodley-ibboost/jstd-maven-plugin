# Introduction #

Add the dependency to your POM:

```
  <dependencies>
       ...
        <dependency>
            <groupId>com.google.jstestdriver</groupId>
            <artifactId>maven-jstestdriver-plugin</artifactId>
            <version>1.3.2.4</version>
            <scope>test</scope>
        </dependency>
        ....
  </dependencies>
```

You might also need to add the following repository and pluginRepository entries:
```
  <repositories>
        <repository>
            <id>jstd-maven-plugin google code repo</id>
            <url>http://jstd-maven-plugin.googlecode.com/svn/maven2</url>
        </repository>
  </repositories>
  <pluginRepositories>
        <pluginRepository>
            <id>jstd-maven-plugin google code repo</id>
            <url>http://jstd-maven-plugin.googlecode.com/svn/maven2</url>
        </pluginRepository>
  </pluginRepositories>
```

Then configure a plugin for your build:
```
        <build>
            ...
            <plugin>
                <groupId>com.google.jstestdriver</groupId>
                <artifactId>maven-jstestdriver-plugin</artifactId>
                <version>1.3.2.4</version>
                <configuration>
                    <port>9876</port>
                </configuration>
                <executions>
                    <execution>
                        <id>run-tests</id>
                        <goals>
                            <goal>jstest</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
        ...
        <build>
```

Finally use it:

```
mvn test
```

Or to run only the JsTestDriver tests:

```
mvn jstestdriver:jstest
```

This assumes you have a persistent instance of the JsTD server running somewhere, and have browsers attached to it.

# More Help #
Check out [Running The Sample App](http://code.google.com/p/jstd-maven-plugin/wiki/RunningTheSampleApp) for a sample app you can use to test your configuration.