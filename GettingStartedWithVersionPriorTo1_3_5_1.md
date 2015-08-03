**NOTE: things have changed as of v1.3.2.5**

The following changes were made in version 1.3.2.5:

  * groupId changed: com.google.jstestdriver -> com.googlecode.jstd-maven-plugin
  * artifactId changed: maven-jstestdriver-plugin -> jstd-maven-plugin
  * goal changed: jstest -> test
  * configuration prefix (when configuring via -D on the command line) changed: jsTestDriver -> jstd

If you are using a version prior to 1.3.2.5, please see [Getting Started With Version Prior To 1.3.2.5](http://code.google.com/p/jstd-maven-plugin/wiki/GettingStartedWithVersionPriorTo1_3_2_5).

# Introduction #

Add the dependency to your POM:

```
  <dependencies>
       ...
        <dependency>
            <groupId>com.googlecode.jstd-maven-plugin</groupId>
            <artifactId>jstd-maven-plugin</artifactId>
            <version>1.3.2.5</version>
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
                <groupId>com.googlecode.jstd-maven-plugin</groupId>
                <artifactId>jstd-maven-plugin</artifactId>
                <version>1.3.2.5</version>
                <configuration>
                    <port>9876</port>
                </configuration>
                <executions>
                    <execution>
                        <id>run-tests</id>
                        <goals>
                            <goal>test</goal>
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
mvn jstd:test
```

This assumes you have a persistent instance of the JsTD server running somewhere, and have browsers attached to it.

# More Help #
Check out [Running The Sample App](http://code.google.com/p/jstd-maven-plugin/wiki/RunningTheSampleApp) for a sample app you can use to test your configuration.