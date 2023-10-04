# Lab 3: Classes and Coroutines

## Resources and Links
* [Unity Learn: Classes](https://learn.unity.com/tutorial/classes-5)
* [Microsoft Learn: Introduction to Classes](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/classes)
* [Learn C#: Classes and Objects](https://www.codecademy.com/learn/build-web-apps-asp-net-intermediate-c-sharp/modules/learn-csharp-classes/cheatsheet)
* [Unity Documentation: Coroutines](https://docs.unity3d.com/Manual/Coroutines.html)
* [Asynchronous Courotines with C#](https://learn.microsoft.com/en-us/events/dotnetconf-2020/asynchronous-courotines-with-c)


## Classes
Classes are reference types that are `null` by default until you explicitly create an instance of the class by using the `new` operator or assign it an object of a compatible type that may have been created elseswhere. 

=== "C#"

``` c# title="DeclaringClasses.cs" linenums="1"
// Declaring an object of type MyClass.
MyClass mc = new MyClass();

// Declaring another object of the same type, assigning it the value of the first object.
MyClass mc2 = mc;

// Classes are declared by using the class keyword followed by a unique identifier
// [access modifier] - [class] - [identifier]
public class Customer 
{
    // Fields, properties, methods and events go here
}

// Objects can be created using the new keyword followed by the name of the class
Customer object1 = new Customer();
    
```
## Class inheritance
Class inheritance means that a class can inherit from any other class that isn't sealed. Other classes can also inherit and override from your class. Classes that inherit must derive from another base class so that it can inherit data and behavior. This base class is specified by appending a colon and the name of the base class bollowing the derived class name. 

In the C# language, a class can only directly inherit from one base class. The class then can directly implement one or more interfaces. 

=== "C#"

``` c# title="ClassInheritance.cs" linenums="1"
// Declaring an object of type MyClass.
public class Manager: Employee
{
    // Employee fields, properties, methods and events are inherited
    // New Manager fields, properties, methods and events go here
}
    
```
## Couroutines
Courtines are really powerful in Unity by how they hook into Unity's core loop by running every frame. When a coroutine, it runs like a function until it reaches a `yield` statment. It then sets a sort of bookmark and `yields`, which tells the rest of the game to proceed. Each frame right after the `Update` function, Unity calls the coroutine again. The coroutine returns to its bookmark and checks its yield condition. When the yield condition is `true`, for exa mple, when 1.5 seconds have passed, the bookmark is deleted and the rest of the coroutine function runs as usual. Coroutines are functions and you call them with the following syntax. 

**When to use couroutines in Unity:**

* Create repeating actions
* To run an animation or play a sound that doesn't change the game state

=== "C#"

``` c# linenums="1"
// Coroutine basic setup
StartCoroutine(PlayFlagpoleAnimation());

IEnumerator PlayFlagpoleAnimation()
{
    // Do stuff
    yield return someCondition;
    // Do more stuff
}
    
```

Below is an example of Unity's built-in `WaitForSeconds` coroutine. While working in Unity, the coroutine you will use the most (by far) is Unity's built-in `WaitForSeconds` coroutine. The `yield` keyword means *keep going with the rest of the game*. Everything after the `return` is called the yield condition. It is something that will eventually be true. For example, afte 1.5 seconds have passed.

=== "C#"

``` c# linenums="1"
// Do stuff
// Then wait
yield return new WaitForSeconds(1.5f);

// Everything after the yield happens after 1.5 seconds
    
```

The coroutine function can have more than one yield statement. It works the same way; the "bookmark" just moves to the latest yield statement. 

=== "C#"

``` c# linenums="1"
// Do stuff
// Then wait 1.5 seconds
yield return new WaitForSeconds(1.5f);

// Do stuff
// Then wait 2 seconds
yield return new WaitForSeconds(2.0f);
    
```

## Try it yourself!
!!! note "Coroutines and Classes"

    Follow along Unity Learn's Intermediate tutorial on [C# Coroutines](https://www.youtube.com/watch?v=5L9ksCs6MbE&ab_channel=Unity). Then watch [Coroutines in Unity](https://www.youtube.com/watch?v=kUP6OK36nrM&t=186s&ab_channel=GameDevBeginner) and [Ienumerator & Corountine in Unity](https://www.youtube.com/watch?v=CU1GHT9tHqQ&ab_channel=DaniKrossing)

    ![Image title](../Labs/Screenshot%202023-10-02%20at%2011.20.39%20AM.png)