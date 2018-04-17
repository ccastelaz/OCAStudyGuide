# OCA Study Guide Summary

"OCA Oracle Certified Associate Java SE 8 Programmer I"
Jeanne Boyarsky and Scott Selikoff. 


## General Exam Evilness
* ***READ EXAM CODE CAREFULLY***

    * Code formatting is frequently less than could be desired, especially in terms of curly braces and scoping.  ***Watch out for tricky one-line `ifs`, and `for` or `while` loops hidden in poorly formatted code.***

    * Pay attention to line numbers in exam code. ***IF THE CODE BEGINS WITH `1:` AND IT DOES NOT CONTAIN A PACKAGE OR IMPORT, THEN THE PACKAGE IS THE DEFAULT, AND THERE ARE NO IMPORTS.*** This may lead to code that will not compile. 

## Chapter 1: Java Building Blocks
* ***Java Building Block Exam Evilness***

    * ***Java keywords are always lowercase.*** Exam code occasionally plays games with capitalization and keywords. For instance, `Public` is a valid variable name because it is capitalized, but `public` is not a valid variable name because it is lowercase, and consequently a keyword.

    * ***Variable names can start with `_`, `$`, or a letter (either case).*** Variable names can not begin with a number.

    * ***`byte`, `short`, `int`, and `long` are signed. The left-most bit carries the sign.***

    * ***Instance and class variables are initialized to default values.*** Local variables are not, and must be explicitly initialized.

    * ***Package names correspond to folders under the current directory.*** For example: if current directory is `~/myproject/src`, the package `com.techelevator` refers to `~/myproject/src/com/techelevator/`.

    * ***A non-static `import` contains a package name followed by a classname, or an asterisk wildcard for all the classes within the package.*** For example: `com.techelevator.Employee` or `com.techelevator.*`. An asterisk may ***not*** appear anywhere else. For example: `com.techelevator.*.Employee` and `com.techelevator.Employee.*` are not valid.

    * ***Do not include the `.class` extension when running an application from the command line.***

    * ***Command line arguments are sperated by spaces.*** Embedded spaces must be quoted, `java Foobar "peanut butter" and jelly`

    * ***Command line arguments are passed into `main` as an array, and consequently, the first argument begins at index zero.***

    * ***Varargs can be used in place of an array provided they appear as the last parameter.***

    * ***Array variables may have `[]` next to the type or the variable name.*** For example: `String[] names[]` and `String names[]` both acceptable, and mean the same thing.
    
    * ***Underscores `_` may be used in `int`, `short`,`long`, `float`, and `double` literals anywhere a comma would normally make sense.*** For example: `1,234`, `1,234.5`, `123,456`, and `123,456.5` are valid. `1,2`, `,1`, `1,.5`, and `1.5,` are ***not*** valid.

* Understanding the Java Class Structure
* Writing a main() Method
* Understanding Package Declaratios and Imports
* Creating Objects
* Distinguishing Between Object References and Primitives

    | Keyword | Type | Max |
    | --- | --- | --- |
    | boolean | true or false | n/a |
    | byte | 8-bit integral value | 0x7F |
    | short | 16-bit integral value | 0x7FFF |
    | int | 32-bit integral value | 0x7FFFFFFF |
    | long | 64-bit integral value | 0x7FFFFFFFFFFFFFFFL |
    | float | 32-bit floating-point value |  |
    | double | 64-bit floating-point value | |
    | char | 16-bit Unicode value | |

* Declaring and Initializing Variables
* Understanding Default Initialization of Variables

    | Type | Default |
    | --- | --- |
    | boolean | false |
    | byte, short, int, long | 0 (in the type's bit-length) |
    | float, double | 0.0 (in the type's bit-length) |
    | char | '\u0000` (NUL)
    | All object references (everything else) | null |

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

    * ***Access modifiers must appear before `class` if used in code.*** For instance, `public class` or `private class`.

    * ***Multiple static and instance blocks and variables are permitted, and can be intermixed.*** They are executed in the order they are written.

* Introducting Class Inheritance
* Creating Abstract Classes
* Implementing Polymorphism

## Chapter 6: Exceptions
* *** Exceptions Exam Evilness ***
    * The question code may contain non-obvious problems such as out of bounds or number formatting exceptions that may change the program flow, or fool you into thinking the question is about something else.  ***IF YOU SEE SOME MENTION OF AN EXCEPTION BEING THROWN IN ONE OR MORE OF THE POSSIBLE ANSWERS, REVIEW THE QUESTION CODE, LOOKING FOR NON-OBVIOUS EXCEPTION(S).*** 

* Understanding Exceptions
    * All exceptions and errors subclass java.lang.Throwable
    * java.lang.Error
        * Catestrophic event, programmer not expected to handle
        * Ex: disk drive mysteriously disappeared
    * java.lang.Exception and any class that subclasses it, except for java.lang.Runtime
        * Checked
        * Programmer must `throws` or handle
        * Ex: Trying to read from a file that doesn't exist
    * java.lang.RuntimeException subclasses java.lang.Exception
        * Unchecked
        * Unexpected, but not necessarily fatal
        * Ex: Indexing an array out of bounds.
    * Programmer-defined exception
        * Extend from java.lang.Exception if you want it "checked"
        * Extend from java.lang.Runtime if you want it "unchecked"
* Using a try Statement
* Recognizing Common Exception Types
* Caling Methods That Throw Exceptions
