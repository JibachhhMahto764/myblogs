---
title: "First Java Program - Input/Output   Part-1"
datePublished: Sat Nov 04 2023 18:16:30 GMT+0000 (Coordinated Universal Time)
cuid: clokd8shf000009ky5al62z39
slug: first-java-program-inputoutput-part-1
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699114095587/142a0028-2f7d-4617-99ad-da9d2e1c3cdf.png
tags: java, developer, hashnode, blogswithcc, wemakedevs

---

## Introduction

**Java** is a versatile, object-oriented programming language known for its platform independence. Java is widely used in web development, mobile app development, desktop applications , and enterprise software. It's also available in open-source implementations like OpenJDK.

In this bloggs we cover alots of things , we look into how to code in java, what is classes, comments and how to code in intellij idea or more

### Creating .java file

In java one things that I mention that every things you gone writing in Java. It's gone be a classes. every files with the extension of .java it's a class itself.

`.java` file involves writing Java code, saving it with a `.java` extension, and compiling it using `javac` . Then, you can run the Java program with the `java` command.

```java
firstprogram.java
```

### Creating Main Function:

The main function basically Means where the program will start. In Java, if there is no main function you will not be able to run the program.

```java
 public static void Main(string[] args){

}
// this is main function in java
```

### Writing first code (print "hello world");

```java

public class Main{
public static void main(string[] args){
System.out.println("Hello World!");
  }
}
```

### Converting .java to .class(Byte Code)

one's you install JDK you will get javac

```basic
~javac Main.java
~java Main

// output: Hello World!
```

### How to change the location of the byte code?

you can change the location where the bytecode (.class files) is generated during compilation by specifying the output directory using the `-d` option with the `javac` command.

```basic
~javac -d /path/to/output/directory YourJavaFile.java
```

\-d flags =&gt; this is basically asking for a particular location where you want to store the bytecode(.class file)

### Starting with Intellij's idea

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1699118372287/dbc2fddd-e3df-4b0e-b9da-4acba956f648.png align="center")

1. **Download and Install IntelliJ IDEA**:
    
    * Visit the official JetBrains website to download IntelliJ IDEA: [https://www.jetbrains.com/idea/download/](https://www.jetbrains.com/idea/download/)
        
    * Run the installer and follow the on-screen instructions to install IntelliJ IDEA.
        
2. **Launch IntelliJ IDEA**:
    
    * After installation, launch IntelliJ IDEA.
        
3. **Configure IntelliJ IDEA**:
    
    When you first start IntelliJ IDEA, you'll be prompted to configure the IDE settings. You can choose the default settings or customize them based on
    
4. Following steps :
    
5. Click project
    
6. Select the latest version
    
7. Open JDK
    
8. Click Project from the Template
    
9. Create a file
    
10. Finish.......
    
    ```java
    package com.jibachh
    public class Main{
    public static void main{Strings[] agrs){
    
    // write your code here
      }
    }
    ```
    

### some Shortcut of Intellij idea:

| Action | Shortcut |
| --- | --- |
| Search everywhere | Double + Shift |
| Go to file | <kbd>Ctrl + Shift + N</kbd> |
| Go to class | <kbd>Ctrl + N</kbd> |
| Go to symbol | <kbd>Ctrl + Alt + Shift + N</kbd> |
| Go to declaration | <kbd>Ctrl + B</kbd> |

# FQA:

1. what is package?
    
    \=&gt; A package is a way to organize and group related classes and interfaces.
    
2. what is system.out.println()?
    
    \=&gt; `System.out.println()` is a Java statement that is used to print text or output to the console.
    
3. what is output in java?
    
    \=&gt; A Printstream adds functionality to another output stream , namely the ability to print representation of various data values, conveniently.
    
4. what is input in java?
    
    \=&gt; "input" refers to the process of obtaining data or information from external sources, typically from the user, a file, a network connection, or another program
    
5. what is class in java?
    
    \=&gt;class in name group of Propertices and function.
    
6. what is static in java?
    
    \=&gt;`static` is used to create variables and methods that belong to the class itself.
    
7. what is public in java?
    
    \=&gt; Public means that this class is access from everywhere.
    
8. what is Main function in java?
    
    \=&gt; the Main function is entry of the java program
    
9. what is void in java?
    
    \=&gt; `void` is a keyword used in method declarations to indicate that the method does not return a value.
    
10. what is main class in java?
    
    \=&gt; Main class in java is just a name of the file name.