<!-- # 🎹 Lab 3: Classes and Coroutines

<div style="width:100%;height:0;padding-bottom:56%;position:relative;"><iframe src="https://giphy.com/embed/29irwFioHzxeyjGLQ0" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/Dumativa-jogo-shieldmaiden-remix-edition-29irwFioHzxeyjGLQ0">via GIPHY</a></p>

## Resources and Links
* [Unity Learn: Classes](https://learn.unity.com/tutorial/classes-5)
* [Microsoft Learn: Introduction to Classes](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/classes)
* [Learn C#: Classes and Objects](https://www.codecademy.com/learn/build-web-apps-asp-net-intermediate-c-sharp/modules/learn-csharp-classes/cheatsheet)
* [Unity Documentation: Coroutines](https://docs.unity3d.com/Manual/Coroutines.html)
* [Asynchronous Courotines with C#](https://learn.microsoft.com/en-us/events/dotnetconf-2020/asynchronous-courotines-with-c)


## Classes
Being the king of the object-oriented world, classes are essential concepts to grasp. Classes are reference types that are `null` by default until you explicitly create an instance of the class by using the `new` operator or assign it an object of a compatible type that may have been created elseswhere. They are some of the most powerful ways to define new types by bundling data (fields) and operations on that data (methods).



**Some important definitions:**

* `Object`: A thing in your software, responsible for a slice of the entire program. They define what information the object must remember and the capabilities it can perform when requested
* `Classes`: Categorized C# objects to establish variables and methods of any object. Think of classes as a blueprint or pattern for objects that belong in a subset
* `Constructor`: Helps new instances that are created by classes, to be ready for use. They are special methods that run when an object comes to life to ensure it begins life in a good state. They must use the same name as the class, and they cannot list a return type

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

    ![Image title](../Labs/Screenshot%202023-10-02%20at%2011.20.39%20AM.png) -->