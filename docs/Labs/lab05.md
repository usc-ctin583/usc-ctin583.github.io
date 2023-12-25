# 🍩 Lab 5: Quaternions

![Image title](../Labs/Fv21c.png)

## Resources and Links
* [Maths - Quaternions](https://www.euclideanspace.com/maths/algebra/realNormedAlgebra/quaternions/)
* [Wolfram: Quaternion](https://mathworld.wolfram.com/Quaternion.html)
* [Unity Documentation: Generic Functions](https://docs.unity3d.com/2019.3/Documentation/Manual/GenericFunctions.html)
* [Microsoft Learn: Generic Classes and Methods](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/types/generics)
* [C# Generics](https://www.programiz.com/csharp-programming/generics)

## Quaternions
In Division Algebra, Quaternions are a method to represent a solid 3D object's three dimensional orientations or other rotational quantity. The algebra for Quaternions consists of 4 dimensions, aka 4 scalar variables that are added and multipled as a single unit. These variables are also known as **Euler Parameters** and hold one real dimension and 3 imaginary dimensions. Each of these imaginary dimensions has a unit value of the square root of -1, but they are different square roots of -1 all mutually perpendicular to each other, known as i,j and k. So a quaternion can be represented as follows:

a + i b + j c + k d 

It may seem strange that there are 3 square roots of -1, but we have to remember that we are working in 4 dimensions so there are at least 3 ways to get round from +1 to -1. It is not very practical to try to draw 4 dimensions in 2 dimensions, but here is an attempt:

The fundamental formula for Quaternion algebra is as follows: 

### Quaternions in Math

### Gimbal Lock

### Rotations in Unity

### Quaternions in Unity
Quaternions are useful in accurately representing rotations. They are compact, don't suffer from gimbal lock and can easily be interpolated. Unity internally uses Quaternions to represent all rotations and expects Quaternions to be normalized. Luckily in Unity, the individual Quaternion components (x,y,z,w) do not need to be individually accessed or modified. You can take the existing rotations and from there, construct new rotations to smoothly interpolate between two rotations. The Quaternion functions that you will use 9% of the time are:

* `Quaternion.LookRotation`
* `Quaternion.Quaternion.Angle`
* `Quaternion.Euler`
* `Quaternion.Slerp`
* `Quaternion.FromToRotation`
* `Quaternion.identity`
* `Quaternion.operator` rotate one rotation by another, or to rotate a vector by a rotation