# Jenkins Status Badges

Status badges for Jenkins builds, strongly inspired by [shields.io](http://shields.io)

![Jenkins Status Badges](http://i.imgur.com/Q6hCHOz.png)

## How to build the plugin

Install Maven, then in the project directory type:

    $ mvn install
    
If you have docker, you can quickly build the plugin without installing Maven:

    $ docker run -it --rm --name jsb -v "$(pwd)":/usr/src/mymaven -w /usr/src/mymaven maven:3.5.3-jdk-8-alpine mvn install

You should get a `status-badges.hpi` in the `target` directory, use the upload form in Jenkins to install it (Jenkins > Plugin Manager > Advanced > Upload Plugin).

## Supported plugins

To get the build informations this plugin is using the API from other plugins.

The followed plugins are currently supported:

* [Clover](http://wiki.jenkins-ci.org/display/JENKINS/Clover+Plugin)
* [Checkstyle](https://wiki.jenkins-ci.org/display/JENKINS/Checkstyle+Plugin)
* [DRY](https://wiki.jenkins-ci.org/display/JENKINS/DRY+Plugin)
