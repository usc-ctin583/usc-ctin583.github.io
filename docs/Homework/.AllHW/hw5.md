# 📔 HW 5: Generics & Inheritence

!!! tip "Assignment Deadline"
    Assignment due **Friday, February 14th** on GitHub

    [Submit :fontawesome-solid-paper-plane:](https://www.gradescope.com/courses/696965/assignments/3876763){ .md-button .md-button--primary }

<div style="width:100%;height:0;padding-bottom:56%;position:relative;"><iframe src="https://giphy.com/embed/70tblROO7cNSqfc188" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/heyduggee-puzzle-hey-duggee-puzzlebadge-70tblROO7cNSqfc188">via GIPHY</a></p>

## Generics

Generics allow us to create code that is more "generic" so that it can be used and reused. Remember **"DRY"** in programming? Also known as **"Don't Repeat Yourself."** Generics are really helpful here in preventing the need for duplicate code - which is always a great thing. They help solve the problem of making classes or methods that would differ only by the types they use, leaving placeholders for types that can be filled in when used.

Generics are created by adding `<T>` after the class name. `<T>` represents the generic type that gets set while being called. We can have multiple generic types in a class by separating them with commas like `<T, U, V>`. When declaring generics in Unity, the general naming convention starts from T and moves alphabetically down as T, U, V, etc. Feel free to make generic methods and gneeric types with multiple type parameters!

To make your life easier, here are some existing and common generic types:

* `Random` generates pseudo-random numbers
* `DateTime` gets the current time and stores time and date values
* `TimeSpan`represents a length of time
* `List<T>` is a popular and versatile generic collection -- use it instead of arrays for most things
* `IEnumerable<T>`is an interface for almost any collection type. The basis for `foreach` loops
* `Dictionary<TKeym, TValue>` can look up one piece of information from another
* `Nullable<T>` is a struct that can express the concept of a missing value for value types
* `ValueTuple` is the secret sauce behind tuples in C#
* `StringBuilder` is a less memory-intensive way to build strings a little at a time

Any type definition that is defined as a generic is a **generic type**. These include classes, structs, or interfaces that leave placeholders the type it uses. They are similar to methods with parameters where they allow programmers to throw in a value. Below is an example of how you would define a generic type. 

=== "C#"

``` c# linenums="1"
// Defining a Generic Type
public class DefineGenericType List<T> {
  private T[] items = new T[0]
  public T Get ItemAt(int index) => items[index];
  public void SetItemAt(int index, T value) => items[index] = value;

  public void Add(T newValue) {
    T[] updated = new T[items.Length + 1];

    for (int index = 0; index < items.Length; index++ ) {
      updated[index] = items[index];
    }

    updated[^1] = newValue;
    items = updated;
  }
}
    
```

When we defined the `DefineGenericType` class above, the `<T>` served as a placeholder for some type. This placeholder type is called a **generic type parameter**. It works just like a method parameter, except it works at a higher leve land stands in for a specific type taht will be chosen later. Conveniently, it can be used throughout the class an in several places in your code. 

=== "C#"

``` c# linenums="1"
// Generic Class Example
public class GenericClass <T> {
  public Type GetMyType() {
    return typeof (T);
  }
}
    
```
The [Unity Scripting API Reference](https://docs.unity3d.com/2023.3/Documentation/ScriptReference/MonoBehaviour.html) documentation lists some functions (for example, the various GetComponent functions) with a variant that has a letter `<T>` or a type name in angle brackets after the function name. These are generic functions. You can use them to specify the types of parameters and/or the return type when you call the function.
=== "C#"

``` c# linenums="1"
void FuncName<T>();
// The type is correctly inferred because it is defined in the function call
var obj = GetComponent<Rigidbody>();
Rigidbody rb = go.GetComponent<Rigidbody>();
    
```
## Inheritence

Class inheritance means that a class can inherit from any other class that isn't sealed. Other classes can also inherit and override from your class. Classes that inherit must derive from another base class so that it can inherit data and behavior. This base class is specified by appending a colon and the name of the base class bollowing the derived class name. Inheritence lets you derive new classes based on existing ones. The new class inherits everything except constructors from the base class. Inheritence is important in accomplishing two things. 

* Enables the treatment of subtypes as the more generalized type
* Consolides code that would have otherwise been duplicated or copy-and-pasted

In the C# language, a class can only directly inherit from one base class. You cannot directly derive from moe than one. The class then can directly implement one or more interfaces. By default, all classes inherit from `object` aka their base class, but you are able to claim a different class as the base class as well. 

=== "C#"

``` c# title="ClassInheritance.cs" linenums="1"
// Declaring an object of type MyClass.
public class Manager: Employee
{
    // Employee fields, properties, methods and events are inherited
    // New Manager fields, properties, methods and events go here
}
    
```

## Resources and Links
* [Unity Learn: Generics](https://learn.unity.com/tutorial/generics#5c8923c5edbc2a113b6bc335)
* [C# Generics and Unity](https://onewheelstudio.com/blog/2020/12/27/c-generics-and-unity)
* [Unity Documentation: Generic Functions](https://docs.unity3d.com/2019.3/Documentation/Manual/GenericFunctions.html)
* [Microsoft Learn: Generic Classes and Methods](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/generics)
* [C# Generics](https://www.programiz.com/csharp-programming/generics)

## Submission

!!! note "GitHub Pull Requests"

    To receive credit for this homework assignment, please make sure you provide a link to your GitHub branch and name the branch as your first name. 
    Then assign Nile and Debbie as `Reviewers` and `Assignees` before you hit the green `Create Pull Request` button.

    ![Image title](../Homework/hw2/notification.png)

    ![Image title](../Homework/hw2/pushtogit.png)

    ![Image title](../Homework/hw2/assignees.png)

!!! note "Kitchen Chaos: Importing Assets"

    Start watching the Kitchen Chaos tutorial from `00:39:30` **Importing Assets**. You are welcome to continue working on the project for as long as you want until the due date but for this homework, please at least watch until `01:42:42`, the end of **Animations** section. You do not have to submit anything on Gradescope for this section. 
    
    <iframe width="560" height="315" src="https://www.youtube.com/embed/AmGSEH7QcDg?si=yngzlEoF3cByBpdz&amp;start=2372" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>