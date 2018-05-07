# Namespaces

## How are name spaces implemented?

Swift uses one root source folder that can access any of the classes/functions in that folder without having to import it.
The only issue is that constants defined on multiple pages can encounter naming collisions. The easy fix to that is to keep static variables in a struct or enum and make a struct or enum with a different name if there were to be any naming collisions.
There are also libraries that can be included with the new swift package manager, and that doesn't apply to the rules listed above. (https://cocoacasts.com/namespaces-in-swift)

A Java package is a named collection of classes that group related elements. According to JAVA in a Nutshell, "Every class has both a simple name, which is the name given to it in its definition, and a fully qualified name, which includes the name of the package of which it is a part." They are implemented with the "import" keyword which allows access to a single Class or entire package using the * operator.

## How are name spaces used?

Swift and Java both use namespaces in order to group together elements in libraries or classes that share similarities. It is useful if, say, two different classes needed to use a static variable of "URL". In Java, each class can have static variables with the same name as another class' static variable. This is not the case in Swift, they must be in different namespaces (different libraries, structs, or enums) because the root source folder shares a namespace.

# Properties

## Getters and Setters

Swift and Java are similar in that certain IDE's such as IntelliJ allow for the automation of getters and setters on private class variables. Getters do not need to use the get keyword. Both languages allow for "Public" variables in classes that can be read and set at will. This is not the safest way to deal with variables in classes, but it is the same in both languages. Swift also allows for the creation of structs that have accessible variables from the start.

## Backing Variables And Computed Properties

In Swift and Java alike, backing variables need to be explicitly declared if needed. In Swift the variable can be initialized in the constructor at the beginning of the class, but the getters and setters have to be declared if one wants to create a computed variable. In Java, computed properties are essentially declared the same way as getters, but the variables is modified within the method. (http://www.dummies.com/programming/macintosh/types-of-swift-properties/)


# Memory Management

## How is it handled?

As a modern, high-level programming language, Swift handles much of the memory management of your apps and allocates or deallocates memory on your behalf using Automatic reference counting. Java has a mixture of automatic and manual reference counting.

## How does it work?

In both Java and Swift the runtime environment keeps track of the reference count of each variable and disposes of it properly when need be. Java has certain elements, however, that need to be manually closed to avoid memory leaks. These can be handled in try, catch, finally blocks and can be more prone to error than automatic reference counting.

## Automatic reference counting and Garbage Collection

Swift handles memory using Automatic Reference Counting, or ARC. This is technically a form of garbage collection, so it does that as well. It does not, however, take care of circular references which would cause memory leaks. (https://www.raywenderlich.com/134411/arc-memory-management-swift)

# Lambda expressions, closures, or functions as types

The creator of Java, James Gosling, expressed displeasure when he looked back on the design of the language. He did not like objects as much as he once had, so lambda expressions were added to the language. According to Jenkov.com, "Java lambda expressions are Java's first step into functional programming. A Java lambda expression is thus a function which can be created without belonging to any class. A lambda expression can be passed around as if it was an object and executed on demand". Swift is different in that it inherently was created with the idea that ie would be a hybrid of functional and object oriented programming. Functions as types and closures were allowed in swift from the beginning, and are now allowed in Java.

# Functional Programming

Java is not known as a functional programming language. Before the release of Java 8, there was no allowance of functional programming. Currently lambda functions are allowed, which was discussed in greater detail in the previous section. Swift does allow functional programming, but also allows object oriented programming. It is a complete hybrid. Java is almost solely an object oriented language, but now has the ability for lambdas.
