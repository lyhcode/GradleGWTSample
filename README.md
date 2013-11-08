## Gradle Build Config for GWT ##

Requirement:

* Gradle (version > 1.0)

Recommended to setup ``PATH`` and ``GRADLE_HOME`` environment variables.
You should have ``gradle`` command visible in you executable PATH.

For Mac OS X and Linux developers, install gradle with ``gvm`` tool is recommended.

* GVM the Groovy enVironment Manager - http://gvmtool.net/

With GVM tool, gradle installation with latest version is very simple to enter:

    gvm install gradle

**Hint.** GWT SDK manually installation is not required.
This build file will download all depedencies with specified GWT version based on settings in ``build.gradle``.

### Configuration ###

First, customize GWT settings in ``build.gradle``

    def gwtVersion = '2.5.1'
    def gwtModule = 'com.example.MyGWTApp'
    def gwtStartupUrl = 'MyGWTApp.html'
    def gwtWarPath = 'war'

The sample contains a GWT default directory structure.
Please ensure the path related settings is fit your project needs.

    /src    # Java Sources
    /war    # WebContents

### Command-line Usages ###

The build.gradle sample defined ``gwtc``, ``devmode`` tasks.
These tasks are equal to GWT official definition in webAppCreator generated build.xml (Ant).

GWT compile to JavaScript (production mode).

    gradle gwtc

Run development mode.

    gradle devmode

Run Jetty web server.

    gradle jettyRun

Package war file.

    gradle war

Compile Java sources only.

    gradle compileJava

Speed up with ``--daemon`` parameter.

    gradle --daemon compileJava

Use gradle with daemon feature, frequently re-run compileJava tasks will save a lot of time.

## Conclusions ##

Build GWT project with Gradle is much better and more convience than Ant.
Gradle build config specfied the GWT version to resolves all dependencies and download automatically.
For future GWT version upgrade, just simply change the version settings.
All the other depdencies for project needs are all configurable.
No more fat JARs need to bundle with project sources.
