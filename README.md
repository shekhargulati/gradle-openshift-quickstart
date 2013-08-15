# Gradle 1.6 OpenShift Quickstart #

This repository will help developers get started with Gradle 1.6 on OpenShift. You can read in detail about it here https://www.openshift.com/blogs/run-gradle-builds-on-openshift.

**Please note that this quickstart is specific to Gradle 1.6. Gradle 1.7 currently does not work with OpenShift. I have raised a issue on Gradle Jira http://issues.gradle.org/browse/GRADLE-2871.**

## Step 1 : Create OpenShift Tomcat 7 application #

```
$ rhc app create gradledemo tomcat-7
```

## Step 2: Pull the source code form github##

```
$ cd gradledemo
$ git rm -rf src/ pom.xml
$ git commit -am "deleted template source code"
$ git remote add upstream -m master https://github.com/shekhargulati/gradle-openshift-quickstart.git
$ git pull -s recursive -X theirs upstream master
```

## Step 3 : Push the source code ##

```
$ git push
```
