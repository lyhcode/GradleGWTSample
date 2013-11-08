## Gradle Build Config for GWT ##

Requirement:

* Gradle (version > 1.0)

Recommended to setup ``PATH`` and ``GRADLE_HOME`` environment variables.
You should have ``gradle`` command visible in you executable PATH.

**Hint.** GWT SDK manually installation is not required.
This build file will download all depedencies with specified GWT version based on settings in ``build.gradle``.

### Configuration ###

Customize GWT settings in ``build.gradle``

    def gwtVersion = '2.5.1'
    def gwtModule = 'com.example.MyGWTApp'
    def gwtStartupUrl = 'MyGWTApp.html'
    def gwtWarPath = 'war'

### Command-line Usages ###

The build.gradle sample defined ``gwtc``, ``devmode`` tasks.
These tasks are equal to GWT official definition in webAppCreator generated build.xml (Ant).

GWT compile to JavaScript (production mode).

    gradle gwtc

Run development mode.

    gradle devmode
