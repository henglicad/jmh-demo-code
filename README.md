# JAVA Microbenchmark Harness (JMH) demo code

This repository provides a simple demonstration of how to use JMH to benchmark source code units (methods). 
The source code file *MyBenchmark.java* implements the code unit to be benchmarked and the configuration of JMH (through Java annotations).
The file *pom.xml* demonstrates how to configute the dependencies of JMH.

## How to run the benchmark

### Step 1: Compile the project
The project is compiled by Maven.
```
mvn clean install
```
The common above will generate two artifacts in the target folder: *benchmark-1.0.jar* (the normal executable of the program) and *benchmarks.jar* (the benchmark version).

### Step 2: Run the benchmark
Execute the benchmark executabe:
```
java -jar target/benchmarks.jar
```

At the end of the execution, there will be a benchmark report like the following one:
```
Benchmark               Mode  Cnt   Score    Error  Units
MyBenchmark.testMethod  avgt    6  ≈ 10⁻³           ms/op
```

For more information please check the official repository of JMH: https://github.com/openjdk/jmh
