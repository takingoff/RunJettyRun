RunJettyRun: Jetty Eclipse Run Configuration Plugin
===================================================

This new version of RunJettyRun is forked from the orginal work done at http://code.google.com/p/run-jetty-run/. Unfortunately the old version has the limitation of only allowing configuration from the plugin dialog and only supporting Jetty6. This new version now supports the ability to supply a jetty.xml configuration file in addition to supporting both Jetty6 and Jetty7.

This version has been tested on Eclipse 3.5 - 3.6. Feedback on whether this works on older versions of Eclipse is encouraged.

Features
---------
- Rebuilt to use Maven2 and eliminated external dependencies
- Easily select between embedded versions of Jetty6 and Jetty7
- Supply jetty.xml file via configuration dialog
- New update site hosted on GitHub

Update Site
------------
- [http://alexwinston.github.com/RunJettyRun/update](http://alexwinston.github.com/RunJettyRun/update)

Quick Start
------------
Simply use Eclipse's update manager (Help -> Install New Software... -> Add... to add a remote site and point it to http://alexwinston.github.com/RunJettyRun/update. Click finish, select the plugin (just one choice) and finish again.

Open "Run Configurations" and add a new "Jetty Webapp". Select between Jetty6 and Jetty7 and then click "Browse" to locate a jetty.xml file on the filesystem or simply type the name of the jetty.xml file for the current project. By default the plugin will look in the project root directory if a path is not specified.

Building
--------
RunJettyRun uses Maven to build the plugin.  Running "mvn package" from the root should build the bootstrap and feature projects and subsequently build the plugin and copy the jar to the site/update/plugin directory.
