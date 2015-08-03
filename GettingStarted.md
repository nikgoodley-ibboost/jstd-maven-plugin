**NOTE: Things have changed as of v1.3.5.1**

The following changes were made in version 1.3.5.1:

  * No longer need to add as a `<dependency>`.
  * No longer need _googlecode.com_ as a repository/plugin repository.

If you are using a version prior to 1.3.5.1, please see [Getting Started With Version Prior To 1.3.5.1](http://code.google.com/p/jstd-maven-plugin/wiki/GettingStartedWithVersionPriorTo1_3_5_1).

If you are using a version prior to 1.3.2.5, please see [Getting Started With Version Prior To 1.3.2.5](http://code.google.com/p/jstd-maven-plugin/wiki/GettingStartedWithVersionPriorTo1_3_2_5).

# Introduction #

Configure the plugin in your _pom.xml_:
```
        <build>
            ...
            <plugin>
                <groupId>com.googlecode.jstd-maven-plugin</groupId>
                <artifactId>jstd-maven-plugin</artifactId>
                <version>1.3.5.1</version>
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

Or to run only the JS Test Driver tests:

```
mvn jstd:test
```

This assumes you have a persistent instance of the JsTD server running somewhere, and have browsers attached to it.

# More Help #
Check out [Running The Sample App](http://code.google.com/p/jstd-maven-plugin/wiki/RunningTheSampleApp) for a sample app you can use to test your configuration.