# Introduction

Within this archive you find the replication package for the paper "Smoke testing and metamorphic testing for classification algorithms" by Steffen Herbold which is currently under review. The aim of this replication package is to allow other researchers to replicate our results with minimal effort. 

# Requirements
- Java 8
- Python 3.5

# Contents
This archive contains:
- The directory generated-tests with the JUnit/unittest test suites that were generated for Weka, scikit-learn and Spark MLlib. 
- The directory test-results with the XML exports of the results of the test executions. 

# How does it work
To replicate the test generation, you require the tool [atoml](https://github.com/sherbold/atoml). The Project contains a gradle file that contains all required Java dependencies, including for the execution of the JUnit tests for Weka and Spark MLlib. Moreover, the project contains a JUnit tests, which can be used for the generation of the test suite ([Weka](https://github.com/sherbold/atoml/blob/master/src/test/java/atoml/WekaTestgenerationTest.java) / [scikit-learn](https://github.com/sherbold/atoml/blob/master/src/test/java/atoml/ScikitTestgenerationTest.java) / [Spark MLlib](https://github.com/sherbold/atoml/blob/master/src/test/java/atoml/SparkTestgenerationTest.java)).

The tests generated tests can be executed using JUnit, resp unittest. For The JUnit test, make sure that Weka (and the plug-ins for classifiers), resp. Spark and Spark ML are part of the classpath for the test execution. For scikit-learn, make sure that the latest version of scikit-learn and numpy are available. 

# License

This replication package is used are licensed under the Apache License, Version 2.0.
