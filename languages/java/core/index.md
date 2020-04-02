- [Getting Started](#getting-started)
  - [Type of Java Application](#type-of-java-application)
    - [Standalone Application](#standalone-application)
    - [Web Application](#web-application)
    - [Enterprise Application](#enterprise-application)
    - [Mobile Application](#mobile-application)
  - [Java Platforms Edition](#java-platforms-edition)
    - [Java SE](#java-se)
    - [Java EE](#java-ee)
    - [Java ME](#java-me)
    - [Java FX](#java-fx)
  - [Features of Java](#features-of-java)
    - [Simple](#simple)
    - [Object Oriented](#object-oriented)
    - [Platform Independent](#platform-independent)
    - [Secured](#secured)
    - [Robust](#robust)
    - [Architecture-neutral](#architecture-neutral)
    - [Portable](#portable)
    - [High-performance](#high-performance)
    - [Distributed](#distributed)
    - [Multi-threaded](#multi-threaded)
    - [Dynamic](#dynamic)
  - [Java Program Execution Internal](#java-program-execution-internal)
  - [Java Setup / Configuration](#java-setup--configuration)
  - [JVM vs JRE vs JDK](#jvm-vs-jre-vs-jdk)
    - [JVM](#jvm)
    - [JRE](#jre)
    - [JDK](#jdk)
  - [Data Types](#data-types)
  - [Operator Precedence](#operator-precedence)
- [Collections](#collections)

# Getting Started

## Type of Java Application

### Standalone Application

- Technologies: 
  - AWT
  - Swing

### Web Application

- Technologies:
  - Servlet
  - JSP
  - Struts
  - Spring
  - Hibernate
  - JSF

### Enterprise Application

- Technologies:
  - EJB

### Mobile Application

- Technologies:
  - Android
  - Java ME

## Java Platforms Edition

### Java SE

- **APIs**: java.lang, java.io, java.net, java.util, java.sql, java.math
- **Topics**: OOPs, String, Regex, Exception, Inner classes, Multithreading, I/O Stream, Networking, AWT, Swing, Reflection, Collection, etc.

### Java EE

- **Topics**: Servlet, JSP, Web Services, EJB, JPA, etc.

### Java ME

- Used to develop mobile applications

### Java FX

- Used to develop rich internet application
- Uses light-weight user interface API

## Features of Java

### Simple

- Syntax is based on C++
- No explicit pointer or operator overloading
- Automatic garbage collection

### Object Oriented

### Platform Independent


### Secured

- **No explicit pointer**
- Java programs `run inside a virtual machine sandbox`
- Classloader
  - Part of JRE used to load java classes into JVM dynamically
  - Adds security by `separating` the package for the classes of the `local file system` from those that are imported from `network sources`
- **Bytecode Verifier**: checks code fragments for illegal code violating access rights to objects
- **Security Manager**: determines `what resources a class can access` such as reading and writing to the local disk

### Robust

- Uses strong memory management
- Lack of pointers that avoid security problems
- Automatic garbage collection
- Exception handling and type checking

### Architecture-neutral

### Portable

- Because it facilitates you to carry the Java bytecode to any platform

### High-performance

- Faster than other traditional interpreted programming languages because Java bytecode is "close" to native code
- Still a little bit slower than a compiled language (e.g., C++)

### Distributed

- RMI and EJB are used for creating distributed applications
- Able to access files by calling the methods from any machine on the internet.

### Multi-threaded

### Dynamic

- Classes are loaded on demand

## Java Program Execution Internal

- You can have different file name and class name only if class is not public

.java  > comile >  .class > ByteCode Verified > Interpreter > Runtime > Hardware

## Java Setup / Configuration

- Download and install JDK
- Set path of JDK\bin directory 
  - Temporary:  `set path=c:\...\jdk\bin`
  - Permanent:
    - Window: Set `jdk\bin` path to user environment variable 'PATH'
    - Linux:  `export PATH=$PATH:/home/jdk/bin/`
- Create Java program
    ```java
    class MyProgram{  
        public static void main(String args[]){  
            System.out.println("My First Program !!");  
        }  
    } 
    ```
- Compile java program using `javac MyProgram.java`
  - Java compiler converts the source code into `byte code`
- Run program using `java MyProgram`

## JVM vs JRE vs JDK

### JVM

- Abstract machine which does not exists physically
- It runs bytecode which might be written in different languages but compiled to bytecode
- JVM is *specification*, *implementation*, and *instance*.

### JRE

- Set of software tools which are used for developing Java applications
- Used to provide the runtime environment
- Implementation of JVM
- Contains set of libraries that is used by JVM at runtime

### JDK

- Contains JRE + development tools
- Contains a private Java Virtual Machine (JVM), interpreter/loader (java), a compiler (javac), an archiver (jar), a documentation generator (Javadoc), etc.

## Data Types

![Data Types](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20191105122725/Primitive-Data-Types-in-Java-4.jpg "Data Types")

## Operator Precedence

![Operator Precedence](https://minigranth.com/wp-content/uploads/2018/06/Operators-in-Java-Comparison.jpg "Operator Precedence")

# Collections

![Java Collections](https://static.javatpoint.com/images/java-collection-hierarchy.png "Java Collections")



> # References

- https://www.javatpoint.com/java-tutorial
