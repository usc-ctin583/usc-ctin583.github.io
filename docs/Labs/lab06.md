# 👷‍♀️ Lab 6: Publishing Builds

## Resources and Links
* [Unity Manual: Publishing Builds](https://docs.unity3d.com/Manual/PublishingBuilds.html)
* [Unity Learn: Create and publish WebGL builds](https://learn.unity.com/tutorial/creating-and-publishing-webgl-builds)
* [YouTube: Create and Publish WebGL Build in Unity](https://www.youtube.com/watch?v=X8Njwk4IRo0&ab_channel=DALAB)
* [YouTube: Publish your Unity game on Google Play Store](https://www.youtube.com/watch?v=UXl_C3ZnRLc&ab_channel=CocoCode)
* [YouTube: How to publish a Unity project to itch.io](https://www.youtube.com/watch?v=fPBv5aflE6Y&ab_channel=MERLINDEV%7CUnityTutorials%26HowTo)


## Builds
<iframe src="https://giphy.com/embed/1K64ALJFeedkcwUc6C" width="480" height="480" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/build-built-memeland-1K64ALJFeedkcwUc6C">via GIPHY</a></p>

During class, we have been running our projects within the Unity Editor. This is a great way to quickly test things and iterate. Now we want players to experience our games! 

What is a **build**? A **build** is a standalone version of your game, so our players don't need to open our projects in Unity. They can double-click on the program to run the game. The term **Build** is used interchangeably with **application** or **executable**. They all mean the same thing. 

It isn't possible to run a Windows application on an OSX device. Same goes for a PlayStation game on an iPhone. Each requires its own special format. The operating system the player is using is referred to as a platform or within Unity, a **build target**. Some examples include:

* PS5
* Windows 10
* Oculus Quest 2
* Android 11
* iOS16

Unity allows developers to build games for a variety of platforms. Exporting your game to some platform is an important part of game development, a task that every game developer will have to do at least once during their career! To test your projects, create a build. To release your game to the public, create development builds by checking the `Development Builds` box.


**Important notes:**

* Install optional modules in Unity Hub
* Easily switch between different platforms but code may look different for each platform
* Must accomodate designing for different platforms and adjust the input system to reflect so
* Create a new folder for your builds. Do not push these buils to GitHub and Perforce
* Sometimes the game within your editor will not look and feel the same as your built game
* It is not recommended to rename the folder name that was automatically generated for you. It might break things. If you want to change the name, make a whole new and separate build
* Be careful and precise as you follow the steps, including all punctuation and capitalization


## Rendering Quality
For each device or platform you build to, it is important to consider the quality and the rendering settings of the game. Feel free to adjust and set a certain quality level for different platforms and levels within the game. This will take some experimentation to get to a setting that works best for your game. Edit the settings under `Edit/Project Settings/Quality`.

![Image title](../Labs/Screenshot%202023-10-08%20at%208.53.04%20PM.png)

## Player Settings
You may also have different build settings for each player. Under `Edit/Project Settings/Player`, you may modify player icons, cursors, and names. You can also modify the splash screen animation!

![Image title](../Labs/Screenshot%202023-10-08%20at%208.53.25%20PM.png)

## Marketing
In 2022, Unity merged with ironSource. ironSource helps bring apps and user experiences by focusing on the app's business expansion in relation to the app economy. ironSource helps with monetization, marketing, analytics, and discovery capabilities that help developers scale their app-based businesses. Unity recommends ironSource  to help you monetize and market your game.

**Resources:**

* [How to Consistently Make Profitable Indie Games](https://www.youtube.com/watch?v=LlAc5sBtGkc&t=506s&ab_channel=BraceYourselfGames)
* [How to Market a Game, Chris Zukowski](https://howtomarketagame.com/)