# 🏡 Lab 4: Generics and Inheritence

<div style="width:100%;height:0;padding-bottom:56%;position:relative;"><iframe src="https://giphy.com/embed/70tblROO7cNSqfc188" width="100%" height="100%" style="position:absolute" frameBorder="0" class="giphy-embed" allowFullScreen></iframe></div><p><a href="https://giphy.com/gifs/heyduggee-puzzle-hey-duggee-puzzlebadge-70tblROO7cNSqfc188">via GIPHY</a></p>

## Resources and Links
* [Unity Learn: Generics](https://learn.unity.com/tutorial/generics#5c8923c5edbc2a113b6bc335)
* [C# Generics and Unity](https://onewheelstudio.com/blog/2020/12/27/c-generics-and-unity)
* [Unity Documentation: Generic Functions](https://docs.unity3d.com/2019.3/Documentation/Manual/GenericFunctions.html)
* [Microsoft Learn: Generic Classes and Methods](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/generics)
* [C# Generics](https://www.programiz.com/csharp-programming/generics)

## Generics

Generics allow us to create code that is more "generic" so that it can be used and reused. Remember **"DRY"** in programming? Also known as **"Don't Repeat Yourself."** Generics are really helpful here in preventing the need for duplicate code - which is always a great thing. 

Generics are created by adding `<T>` after the class name. `<T>` represents the generic type that gets set while being called. We can have multiple generic types in a class by separating them with commas like `<T, U, V>`. When declaring generics in Unity, the general naming convention starts from T and moves alphabetically down as T, U, V, etc. 

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