A Maven plugin that allows you to easily integrate your [JS Test Driver](http://code.google.com/p/js-test-driver/) test suite into the Maven build process.

**Please see the [Getting Started](http://code.google.com/p/jstd-maven-plugin/wiki/GettingStarted) page for instructions on use!**

## Updates ##
  * 2/27/2013
    * Version 1.3.5.1 has been released! Changes include:
      * Update to JS Test Driver 1.3.5 (which resides in Maven Central now).
      * No longer have to redundantly specify the plugin as a dependency in the `<dependencies>` tag, only as a `<plugin>`.
      * No longer need to add google code as a repository as everything now resides in Maven Central.
      * Fixed an issue where output gets put in the wrong place when running from a multi-module POM.
    * Be sure to read the [Getting Started](http://code.google.com/p/jstd-maven-plugin/wiki/GettingStarted) page to see how these changes affect you.
  * 2/25/2013
    * I, Nathan Redding, have taken over maintenance on this project. I know it's been a long time coming, so very soon there will be a new version with the latest version of JSTD. I also hope to have a few other minor improvements which you will discover shortly! I'm mostly waiting on Sonatype to create a new project for me which will enable me to host build artifacts instead of relying on Google Code. Keep checking back for updates!
  * 8/9/2011
    * Released 1.3.2.5
      * Repackaged everything into org.googlecode.jstd-maven-plugin:jstd-maven-plugin in order to get this into the central repo.
      * See the [Getting Started](http://code.google.com/p/jstd-maven-plugin/wiki/GettingStartedWithVersionPriorTo1_3_5_1) wiki page for a full list of the changes.
  * 8/8/2011
    * Working on getting the dependencies into the central repo - https://issues.sonatype.org/browse/OSSRH-2044
    * Released 1.3.2.4 - Fixing [issue 8](https://code.google.com/p/jstd-maven-plugin/issues/detail?id=8) - now defaulting basePath
    * Released 1.3.2.3 - Fixing [issue 9](https://code.google.com/p/jstd-maven-plugin/issues/detail?id=9)
    * converting repo over to git
  * 4/5/2011 - Working on getting the jstestdriver jar's uploaded as 3rd party artifacts into Maven central.
  * 4/4/2011
    * Released 1.3.1 and 1.3.2 snapshots.
      * There is an issue when using 1.3.2 with the sample-app. It seems relative file paths are broken as of jstd 1.3.2.  Things will not work properly until the issue is fixed by the jstd project.
    * Released 1.3.1.1 and 1.3.2.1 release versions of the plugin.
  * 2/23/2011 - Beginning work to support v1.3.
  * 8/13/2010 - Recreated the maven repository under svn/maven2 instead of the older svn/repo.  You will want to update your paths accordingly.