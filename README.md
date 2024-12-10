# HelloWorld.java

![thumbnail](./Thumbnail.jpeg)

Welcome to the **Nanowar Of Steel**'s first GitHub project, and first ever example of a **source-code song**.
The aim of this project is to support and enforce "_True metal programming_", that basically means: "_write code so badly that only you can sing it_".

You can find the source-code video in the link below:
https://www.youtube.com/watch?v=yup8gIXxWDU

[Here](https://nanowar.it/) is the Nanowar Of Steel official website.

[Here](https://www.youtube.com/@nanowarVEVO) is the Nanowar Of Steel Youtube Channel.

Some important notes:
1. Beware of ```Joey De Caio```, if set to null It may suddenly cancel the program execution with a NullPointerException.
2. ```metal``` variable is very important! If it is set to "false", it may trigger the Joey De Caio variable mentioned above.
3. ```tizio``` and ```foo``` are very close friends.
4. ```pippo``` isn't ```tizio```'s friend, but he's been flirting with ```foo```.
5. In the comments "**manage**" should be renamed as "**handle**" (we all wish "manage" was the right word, but it's not).
6. The constructor argument is used to control the number of executions. However, It may be completely useless if the execution is cancelled by ```Joey De Caio```.
7. "_Write once, run anywhere_" means literally anywhere (e.g. Hellfest).
8. ```songRefrain()``` identifies itself as a void method.

Below you will find a super detailed guide to the program, of course written with ChatGPT.

---

# HelloWorldMainLauncherClass

This project contains a simple Java application that demonstrates the basic usage of loops, conditionals, and handling null-pointer exceptions. The main functionality includes printing "Hello World!" multiple times based on a user-defined parameter and intentionally introducing a bug to highlight error handling.

## Overview

The `HelloWorldMainLauncherClass` performs the following tasks:

1. **Initialization**: Accepts an integer parameter (`foo`) that controls how many times "Hello World!" will be printed.
2. **Song Refrain**: Prints "Hello World!" twice—first using a `for` loop and then using a `while` loop.
3. **Exception Handling**: Contains a method `falseMethod()` that introduces a `NullPointerException` by calling `length()` on a `null` string to simulate error handling.

## Features

- **Hello World printing**: Outputs the message "Hello World!" a number of times based on the provided parameter.
- **Loops**: Demonstrates basic usage of `for` and `while` loops in Java.
- **Exception simulation**: Introduces a `NullPointerException` for demonstration purposes.
- **Basic Java structure**: Showcases constructor usage, instance variables, and method definitions.

## Prerequisites

- Java Development Kit (JDK) 8 or higher.
- A Java IDE (like IntelliJ IDEA, Eclipse, or NetBeans) or a command-line environment to compile and run the Java program.

## Installation

To set up and run this project locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/NanowarOfSteel/HelloWorld.git
   ```

2. Navigate into the project sources directory:
   ```bash
   cd HelloWorld/src/main/java
   ```

3. Compile the Java file:
   ```bash
   javac it/nanowar/ofsteel/helloworld/HelloWorldMainLauncherClass.java
   ```

4. Run the program:
   ```bash
   javac it/nanowar/ofsteel/helloworld/HelloWorldMainLauncherClass.java
   ```

Alternatively, with Java 11 you can compile and run the project in one single step:

3. Compile and run the Java file:
   ```bash
   java it/nanowar/ofsteel/helloworld/HelloWorldMainLauncherClass.java
   ```

## Usage

Once you run the program, you will see the following output:

```
Hello World Programmer Start
Hello World!
Hello World!
Hello World!
Hello World!
Program Finished!
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.length()" because "joeyDeCaio" is null
    at HelloWorldMainLauncherClass.falseMethod(HelloWorldMainLauncherClass.java:35)
    at HelloWorldMainLauncherClass.main(HelloWorldMainLauncherClass.java:27)
```

### Configuration

The number of times "Hello World!" is printed can be controlled by changing the parameter passed to the constructor of `HelloWorldMainLauncherClass`. For example:

```java
HelloWorldMainLauncherClass tizio = new HelloWorldMainLauncherClass(3);
```

This will print "Hello World!" three times.

## Code Explanation

1. **Constructor**: The constructor takes an integer `foo` that determines how many times the message will be printed.
   ```java
   public HelloWorldMainLauncherClass(int foo) {
       super();
       this.foo = foo;
   }
   ```

2. **songRefrain() Method**: The method contains two loops—`for` and `while`—both of which print "Hello World!" the number of times specified by `foo`.
   ```java
   public void songRefrain() {
       for (int i = 0; i < foo; i++) {
           System.out.println("Hello World!");
       }

       int pippo = 0;
       while (pippo < foo) {
           System.out.println("Hello World!");
           pippo++;
       }
   }
   ```

3. **falseMethod() Method**: This method deliberately introduces a bug by attempting to call `length()` on a `null` string.
   ```java
   public void falseMethod() {
       boolean metal = false;
       if (metal == false) {
           String joeyDeCaio = null;
           joeyDeCaio.length();
       }
   }
   ```
### Notes:

- **Bug introduction**: The purpose of `falseMethod()` is to demonstrate a scenario where an exception is thrown. The `NullPointerException` is handled by the JVM, but no explicit exception handling is implemented in this case.
  
- **Extending the Program**: You can extend the program by adding more features like exception handling, more complex message outputs, or additional loops and conditionals.

# JBang Guide

This repository contains a jbang catalog that allows you to run the HelloWorld program with the command `jbang hello@nanowarofsteel/hello`.

## Table of Contents
- [Prerequisites](#jbang-prerequisites)
- [Usage](#jbang-usage)

## JBang Prerequisites

To use the jbang catalog, you need to have jbang installed. You can install jbang [here](https://www.jbang.dev/download/).

## JBang Usage

To run the HelloWorld program with `jbang`, you can use the following command directly without cloning the repository:

```bash
jbang hello@nanowarofsteel/HelloWorld
```

If you have cloned the repository, you can run the program with the following command:

```bash
jbang hello
```

# Docker Guide

This repository contains a Dockerfile that automates the process of building and running a Java application using Maven. The Docker image is built in two stages: the first stage builds the application with Maven, and the second stage runs the application with a minimal OpenJDK 17 image.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Build and Run Instructions](#build-and-run-instructions)
- [Usage](#usage)
- [Cleaning Up](#cleaning-up)
- [Notes](#notes)
- [Performance considerations](#performance-considerations)

## Prerequisites

Before building and running the Docker image, make sure you have the following installed:

- **Docker**: [Install Docker](https://www.docker.com/get-started)
- **Maven**: (Optional) Maven is only needed locally for building the project if you're not using the Docker build.

## Build and Run Instructions

### 1. Clone the repository

First, clone the repository containing the project and the Dockerfile to your local machine:

```bash
git clone https://github.com/NanowarOfSteel/HelloWorld.git
cd HelloWorld
```

### 2. Build the Docker image

You can build the Docker image using the following command. Make sure you're
in the root directory of the project, then point out the location of the
Dockerfile with the `-f` option:

```bash
docker build -t my-java-app -f src/main/docker/helloworld.dockerfile .
```

This command will:
1. Use an official Maven image to build the application.
2. Package the application into a JAR file.
3. Use a slim OpenJDK 17 image to run the resulting application (**kinda**).

## Usage

After the build is complete, you can run the Docker container using:

```bash
docker run --rm my-java-app
```

## Cleaning Up

If you didn't use the option `--rm` when instanciating the container, you will
have to manually remove the container and image once you're done:

```bash
docker rm <container_id>  # Remove the container
docker rmi my-java-app    # Remove the image
```

## Notes

- **Multi-stage build**: The Dockerfile uses a multi-stage build to ensure the final image is small and optimized for running the application. The first stage uses the Maven image to build the application, and the second stage uses a slim JDK image to run it.
- **JAR file location**: The final JAR file is copied from the `/target` directory in the Maven build stage to the working directory in the runtime stage (`/app`).

## Performance considerations

In order to achieve better performance experience this code live.
Due to resource allocation issues there are only limited possibilities:

- FRIDAY 21 FEBRUARY 2025: Vienna, Austria - Simm City

- SATURDAY 22 FEBRUARY 2025: Leipzig, Germany - Hellraiser

- SUNDAY 23 FEBRUARY 2025: Stuttgart, Germany - Halle, Im Wizemann

- MONDAY 24 FEBRUARY 2025: Hamburg, Germany - Kaiserkeller (Grosse Freiheit)

- WEDNESDAY 26 FEBRUARY 2025: Paris, France - La Machine du Moulin Rouge

- THURSDAY 27 FEBRUARY 2025: Pratteln, Switzerland - Z7 Konzertfabrik

- FRIDAY 28 FEBRUARY 2025: Villeurbanne, France - La Rayonne

- SATURDAY 1 MARCH 2025: Lindau, Germany - Club Vaudeville

- SUNDAY 2 MARCH 2025: Nuremberg, Germany - HIRSCH

- TUESDAY 4 MARCH 2025: Aarhus, Denmark - VoxHall

- WEDNESDAY 5 MARCH 2025: Tilburg, Netherlands - 013

- THURSDAY 6 MARCH 2025: Frankfurt, Germany - Zoom Frankfurt

- FRIDAY 7 MARCH 2025: Wrocław, Poland - Transformator

- SATURDAY 8 MARCH 2025: Budapest, Hungary - Barba Negra

- SUNDAY 9 MARCH 2025: Krakow, Poland - Kwadrat

- MONDAY 10 MARCH 2025: Berlin, Germany - Columbia Theater

- WEDNESDAY 12 MARCH 2025: Antwerp, Belgium - Kavka Zappa

- FRIDAY 14 MARCH 2025: Drachten, Netherlands - Poppodium Iduna

- SATURDAY 15 MARCH 2025: Strasbourg, France - Le Molodoï

- FRIDAY 4 - SATURDAY 5 APRIL 2025: epic fest denmark 2025:  - Roskilde-Hallerne, Roskilde, Denmark

Further information about upcomming resources can be found here: https://www.nanowar.it/live/

  
## Troubleshooting

- **Issue**: The application isn't starting or doesn't work as expected.
  - **Solution**: Check the logs for any error messages by running:
    ```bash
    docker logs <container_id>
    ```

- **Issue**: Docker build fails due to missing dependencies.
  - **Solution**: Make sure all necessary dependencies are listed in your `pom.xml` file, and try running `mvn clean install` locally to check for issues before attempting the Docker build.

---
## Docker compose guide

## Prerequisites 

- Docker: [Install Docker](https://www.docker.com/get-started)
- Docker compose: [Install Docker Compose](https://docs.docker.com/compose/install)

## Build and Run Instructions 

### 1. Clone the repository 

Do as described in [Docker Build and Run Instructions](#1-clone-the-repository)

### 2. Build and Run

With Docker Compose building and running are done with one command (run in the project root):

```bash
docker compose up
```


This command will build and run the project serving it on port 8080.

For further explanations see the comments in file: _docker-compose.yaml_

By running `docker compose up` the output will be captured by the execution.

You can pass the execution context to the docker daemon by running

```bash
docker compose up -d
```

## Cleaning Up

If you ran `docker compose` without the `-d` flag stop the execution by pressing `ctrl+c`

If you ran `docker compose -d` you can stop the execution by running 

```bash
docker compose down
```

within the directory where the file _docker-compose.yaml_ is located

Run

```bash
docker compose rm
```

to remove the stopped container.

Then do as describe in [Cleaning Up for Docker](#cleaning-up) except for the remove the stopped container part

## Troubleshooting (only for Mac or Linux)

If you get this error:
`Error response from daemon: driver failed programming external connectivity on endpoint helloworld-app-1 (1769c92017f2d2da48adc989bd2321855e3152f6a11932c18ed36e7df443f0ae): failed to bind port 0.0.0.0:8080/tcp: Error starting userland proxy: listen tcp4 0.0.0.0:8080: bind: address already in use'
`

It means the port 8080 is already binded (maybe by the previous docker execution without cleaning up).

To solve it find the process running on port 8080 by running

```bash
lsof -i tcp:8080
```

Note the `PID` value of the output and kill the process by running 

```bash
kill <PID>
```


---

# License

This project is licensed under the IronAvantgarde Publishing & Napalm Records License - see the [Napalm Records Website](https://napalmrecords.com/) for more details.

# Contributing

Feel free to fork this repository, submit issues, or open pull requests if you'd like to improve this code. Contributions are always welcome!

# Contacts

**Do you want some buggy, personalized and singable code by Nanowar Of Steel**? Please contact us [here](mailto:nanowar@nanowar.it). 
