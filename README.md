# Tycho Archetype

[![Build Status](https://travis-ci.org/KazeJiyu/kazejiyu-tycho-archetype.svg?branch=master)](https://travis-ci.org/KazeJiyu/kazejiyu-tycho-archetype) [![Bintray](https://img.shields.io/bintray/v/kazejiyu/kazejiyu-tycho-archetype/kazejiyu-tycho-archetype.svg)](https://bintray.com/kazejiyu/kazejiyu-tycho-archetype)

A [Maven Archetype](https://maven.apache.org/guides/introduction/introduction-to-archetypes.html) that can be used to generate the architecture of a [Tycho](https://www.eclipse.org/tycho/) project.

## Sample project 

This repository contains a [sample project](src/test/resources/projects/piou/reference) that can be looked up to see how a project generated by this archetype looks like.

## Usage

### Installing

As any other archetype, the Tycho Archetype can be used from the command line. It is identified by the following properties:

**groupId**: fr.kazejiyu.maven.archetypes  
**artifactId**: kazejiyu-tycho-archetype  

> Please check GitHub badges above for the latest version.

Type the following command to use the archetype:
```
mvn archetype:generate -DarchetypeGroupId=fr.kazejiyu.maven.archetypes -DarchetypeArtifactId=kazejiyu-tycho-archetype -DarchetypeVersion=0.1.0 -DarchetypeRepository=https://dl.bintray.com/kazejiyu/maven
```

> You can alternatively clone this repository then install the archetype in your local installation by typing `mvn install`

## Generated files

The archetype follows [Lars Vogel advices](http://www.vogella.com/tutorials/EclipseTycho/article.html) on how a Tycho project should be structured. More specifically, it generates the following architecture:

```
│   pom.xml
│
├───.mvn
│       extensions.xml
│
├───bundles
│       pom.xml
│
├───features
│       pom.xml
│
├───releng
│   │   pom.xml
│   │
│   ├───<artifactId>.releng.configuration
│   │       .project
│   │       pom.xml
│   │
│   ├───<artifactId>.releng.p2
│   │       .project
│   │       category.xml
│   │       pom.xml
│   │
│   └───<artifactId>.releng.targetplatform
│           .project
│           <artifactId>.releng.targetplatform.target
│           pom.xml
│
└───tests
        pom.xml
```
