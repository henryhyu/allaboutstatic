# all about static
"Static" Defined (in java)!

TLDR: The static keyword denotes that a member variable, or method, can be accessed without requiring an instantiation of the class to which it belongs.

In simple terms, it means that you can call a method, even if you've never created the object to which it belongs! Every time you run a stand-alone application (which requires a static main method), the virtual machine can call the main method without creating a new application object. Of course, unless the application's methods are all static, you will need to create an instance of it at some point.

Benefits: It makes your program memory efficient (i.e it saves memory).
Java static property is shared to all objects.

The static keyword in java is used for memory management mainly. We can apply java static keyword with variables, methods, blocks and nested class. The static keyword belongs to the class instead of a specific instance of the class.

The static can be:

variable (also known as class variable)

method (also known as class method)

block

nested class

Purpose: Utility is a good keyword for static. You do not want to create instances of yourself, so you make it a function/functionality. If you put something to be static, it is like making it a function of a class.

If it is not static, you want it to be object oriented, like a blueprint, a map, so that others can be instances of it. 
If you have a non static method, then you want to create instances of it, which means you have instance variables too to manipulate

Classes that contain static and non static methods provide utility to manipulate itself

Static methods do not use instance variables of any object of the class they are defined in. Static methods typically take all their data from parameters and compute something from those parameters, with no reference to variables. This is typical of methods which do some kind of generic calculation. A good example of this are the many utility methods in the predefined Math class. 
Static Methods can access class variables without using object of the class. It can access non-static methods and non-static variables by using objects. Static methods can be accessed directly in static and non-static methods. Static variables are also known as Class Variables.

A static class means that you cannot use it in a non-static context, meaning that you cannot have an object instantiation of that class and call the method. A Class can be made static only if it is a nested Class. The nested static class can be accessed without having an object of outer class.

Ex. 
calling a static method using a class name

•		Math.min(88,86)

calling a non-static method using a reference variable name

•		Song t2 = new Song();

•		t2.play();

Static members belong to the class instead of a specific instance.

It means that only one instance of a static field exists even if you create a million instances of the class or you don't create any. It will be shared by all instances.

Since static methods also do not belong to a specific instance, they can't refer to instance members (how would you know which instance Hello class you want to refer to?). static members can only refer to static members. Instance members can, of course access static members. Side note: Of course, static members can access instance members through an object reference.
```
public class Example{

    private static boolean staticField;
    private boolean instanceField;
    public static void main(String[] args) {
       
       
        // a static method can access static fields
        staticField = true;
        // a static method can access instance fields through an object reference
        Example instance = new Example();
        instance.instanceField = true;
    }

```
