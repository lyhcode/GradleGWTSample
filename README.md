## Gradle Build Config for GWT ##

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
