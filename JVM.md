# Java Virtual Machine (JVM)
### Introduction
- an abstract machine 
- runtime environment to execute java bytecode 
- platform dependent
### Defintion of JVM
Its <br>
1. **A specification** :
    - specified place for java machine code. 
    - implementation provider is independent to choose the algorithm. 
    - implementations provided by Oracle and other companies 
2. **An implementation** :
    - Implementation of JVM is JRE(Java Runtime Environment)
3. **Runtime Instance** :
    - while running java class programs an instance of JVM is created. 
---
### Functions of JVM
JVM performs:
- Loads code 
- Verifies code 
- Executes code 
- Provides runtime environment

JVM provides definitions for :
- Memory area
- Class file format 
- Register set 
- Garbage-collected heap
- Fatal error reporting

----
### Architecture of JVM
<img src="https://static.javatpoint.com/images/jvm-architecture.png" alt="JVM structure" height="500px" align="center">
<br>
Internal architecture of JVM is made of classloader,memory area, execution engine etc.

1. **Classloader**:
    - subsystem of JVM used to load class files. 
    - program first loaded by the classloader while running the program 
    - main functionality is **Loading**, **Linking** & **Initalization**.
    - **Loading**: following informations are checked when a classloader reads the ".class" file, 
        - fully qualified name of the loaded class and its immediate parent class.
        - Whether the ".class" file is related to Class or Interface or Enum.
        - Modifier,Variables and Method information etc.
    - **Linking** also happens here, while linking main fucntions are : <br>
        - **Verification**: 
            - checking of classfile (format & validity) if check failed returns run-time exception `java.lang.VerifyError`.
            - Done mostly by the ByteCodeVerifier.
        - **Preparation**: 
            - JVM allocates memory for class variables and initalizing the memory to default values
        - **Resolution**: 
            - Porcess of replacing symbolic references from type with direct reference. 
            - done by searching into the method area to locate the referenced entity.
    - **Initalization**: 
        - static variables are assigned with their values defined in code and static block (if any).
        - executed from top to bottom in a class 
        - executed from parent to child in the class hierarchy.

    - there are three buit-in classloaders: 
 - **Bootstrap ClassLoader** : 
    - first classloader, super class of Extension classloader. 
    - loading of class files is done here 
    - loads **`rt.jar`** file which contains all class files of JavaSE 
    
 - **Extension ClassLoader** :
    - child classloader of Bootstrap & parent classloader of System classloader 
    - loads the jar files located inside **`$JAVA_HOME/jre/lib/ext`** directory.
 - **System/Application ClassLoader** :
    - child classloader of Extension classloader. 
    - loads the classfiles from classpath. 
    - by default set to current directory.
    - can change classpath using "-cp" or "-classpath" switch also known as Application classloader.
<img src="https://media.geeksforgeeks.org/wp-content/uploads/jvmclassloader.jpg" alt="classloader" height="300px" align="center">
 
