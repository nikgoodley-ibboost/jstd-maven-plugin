# Introduction #

A sample app can be found in the sample-app directory.  You can use this to experiment and play with the setup and use of both JsTD and this plugin.

# Steps #

## Get the source ##
Checkout out the source via git:

```
git clone https://code.google.com/p/jstd-maven-plugin/ jstd-maven-plugin
```

## Install the plugin snapshot ##
```
cd jstd-maven-plugin
mvn install
```

This will install the jstd-maven-plugin in your local .m2 repository.

## Run the tests ##
```
cd sample-app
mvn test
```

This will start up the JsTD server on port 9876, start and capture your default browser, and then run the tests.

The sample assumes you are running in Mac OS X.  If this is not true, you will have to adjust the `<`browser`>` setting to point to the browser executable you wish to use.