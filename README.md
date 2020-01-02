# maven-repository
This project is to release TeamVK's publicly released Java resouces in the form of Maven repository.

## How to use 
In order to use this maven repository, you can use various plugins (for your build system such as Gradle and Maven).

### Gradle
Add somethign like the following to your build.gradle script.

```
plugins {
    id "com.github.unafraid.gradle.git-repo-plugin" version "2.0.4.1"
    id "java"
    id "maven-publish"
}

apply plugin: "com.github.unafraid.gradle.git-repo-plugin"

repositories {
    jcenter()
    mavenCentral()
    github("teamvk", "maven-repository", "origin", "master", "release")
}

```
