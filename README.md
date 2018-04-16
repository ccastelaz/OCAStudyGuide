# OCA Study Guide Summary

"OCA Oracle Certified Associate Java SE 8 Programmer I"
Jeanne Boyarsky and Scott Selikoff. 


## General Exam Evilness
* ***READ EXAM CODE CAREFULLY***
    * Code formatting is frequently less than could be desired, especially in terms of curly braces and scoping.  ***Watch out for tricky one-line `ifs`, and `for` or `while` loops hidden in poorly formatted code.***
    * Pay attention to line numbers in exam code. ***IF THE CODE BEGINS WITH `1:` AND IT DOES NOT CONTAIN A PACKAGE OR IMPORT, THEN THE PACKAGE IS THE DEFAULT, AND THERE ARE NO IMPORTS.*** This may lead to code that will not compile. 

## Chapter 1: Java Building Blocks
* ***Java Building Block Exam Evilness***
    * Java keywords are always lowercase. ***Exam code and/or answers occasionally use capitalized keywords to throw you off.***

* Understanding the Java Class Structure
* Writing a main() Method
* Understanding Package Declaratios and Imports
* Creating Objects
* Distinguishing Between Object References and Primitives
* Declaring and Initializing Variables
* Understanding Default Initialization of Variables
* Understanding Variable Scope
* Ordering Elements in a Class
* Destroying Objects
* Benefits of Java

## Chapter 2: Operations and Statements
* Understanding Java Operators
* Working with Binary Arithmatic Operators
* Working with Unary Operators
* Using Additional Binary Operators
* Understanding Java Statements
* Understanding Advanced Flow Control

## Chapter 3: Core Java API
* Creating and Manipulating Strings
* Using the StringBuilder Class
* Understanding Equality
* Understanding Java Arrays
* Understanding an Arraylist
* Working with Dates and Times

## Chapter 4: Methods and Encapsulation
* Designing Methods
* Working with Varargs
* Applying Access Modifiers
* Passing Data Among Methods
* Overloading Methods
* Creating Constructors
* Encapsulating Data
* Writing Simple Lambdas

## Chapter 5: Class Design
* ***Class Design Exam Evilness***
    * ***Multiple static and instance blocks and variables are permitted, and can be intermixed.*** They are executed in the order they are written.

* Introducting Class Inheritance
* Creating Abstract Classes
* Implementing Polymorphism

## Chapter 6: Exceptions
* *** Exceptions Exam Evilness ***
    * Non-obvious exceptions such as out of bounds or number formatting exceptions. May be missed, and fool you into thinking te question is about something else.  ***LOOK FOR SOME EXCEPTION THROWN IN THE ANSWERS.*** 
    
* Understanding Exceptions
    * All exceptions and errors subclass java.lang.Throwable
    * java.lang.Error
        * Catestrophic event, programmer not expected to handle
        * Ex: disk drive mysteriously disappeared
    * java.lang.Exception and any subclasses except java.lang.Runtime
        * Checked
        * Programmer must `throws` or handle
        * Ex: Trying to read from a file that doesn't exist
    * java.lang.RuntimeException subclass java.lang.Exception
        * Unchecked
        * Unexpected, but not necessarily fatal
        * Ex: Indexing an array out of bounds.
    * Programmer-defined exception
        * Extend from java.lang.Exception if you want it "checked"
        * Extend from java.lang.Runtime if you want it "unchecked"
* Using a try Statement
* Recognizing Common Exception Types
* Caling Methods That Throw Exceptions
