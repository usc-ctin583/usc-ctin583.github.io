# USC CTIN 583: Game Development 👾
hi
This course teaches the art of creating digital game prototypes and introduces the world of game engines. The class briefly introduces industry standard game engines such as Unreal Engine and Godot then dives deep into the Unity game development using C# scripting. In class, students will be creating two games with Unity 3D and Unity AR while learning the fundamentals of C# scripting. This content is open-source and free to the public. If you're interested in learning, please visit our course [website](https://usc-ctin583.github.io/).

* Adjunct Assistant Professor: Deborah Yuen
* Student Assistant: Hao Liu

<img width="1280" alt="Screenshot 2023-08-27 at 12 04 39 PM" src="https://github.com/usc-ctin583/usc-ctin583.github.io/assets/31296177/b5869a03-8fc1-425b-8521-8f6ad3e05bc6">

## Course Requirements  
  * [Godot 4.1](https://godotengine.org/article/godot-4-1-is-here/)
  * [Unreal Engine 5](https://www.unrealengine.com/en-US/unreal-engine-5)
  * [Unity Editor Version 2021.3.29f1](https://docs.unity3d.com/560/Documentation/Manual/InstallingUnity.html)
  * [Git](https://git-scm.com/)
  * [Git LFS](https://git-lfs.com/)
  * [Perforce Helix Core (P4V)](https://www.perforce.com/downloads/helix-visual-client-p4v)
    
## Course Website Set Up

Fork or clone the repo
```bash
$ git clone https://github.com/usc-ctin583/usc-ctin583.github.io.git
```

Check Python is installed
```bash
$ python --version
```

Install MkDocs
```bash
$ pip install mkdocs
```

Check MkDocs is installed
```bash
$ mkdocs --version
```

Install Material for MkDocs
```bash
$ pip install mkdocs-material
```

Run and build Website
```bash
$ mkdocs serve
```

Run with the different versions. See @squidfunk's example [here](https://github.com/squidfunk/mkdocs-material-example-versioning/tree/master).
```bash
$ mike deploy --push --update-aliases 0.1 latest
$ mike set-default --push latest
$ mike deploy --push --update-aliases 0.2 latest
```

If you encounter this error:
```
error: failed to push branch gh-pages to origin:
  To https://github.com/usc-ctin583/usc-ctin583.github.io.git
   ! [rejected]          gh-pages -> gh-pages (fetch first)
  error: failed to push some refs to 'https://github.com/usc-ctin583/usc-ctin583.github.io.git'
  hint: Updates were rejected because the remote contains work that you do not
  hint: have locally. This is usually caused by another repository pushing to
  hint: the same ref. If you want to integrate the remote changes, use
  hint: 'git pull' before pushing again.
  hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

Try:
```bash
$ git branch -D gh-pages
$ git push origin :gh-pages
$ mkdocs build --clean
```

## Usage
Fork this GitHub repo to build upon this course or create next year's website.

## Credits and References
Thank you to prior instructors who helped shape this course. This website was created by Debbie (yuend@usc.edu). 
