# ![[linux.png|35]] C++ setup for Linux (Arch)
---
## The compiler

There is different [[C++]] compilers, ([GCC](https://en.wikipedia.org/wiki/GNU_Compiler_Collection), [Clang](https://en.wikipedia.org/wiki/Clang), [Visual C++](https://en.wikipedia.org/wiki/Visual_C%2B%2B)), I will focus on the *Gnu Compiler Collection* [GCC (g++)](https://en.wikipedia.org/wiki/GNU_Compiler_Collection) because it's FOSS and it's available on the most platforms.

The [GCC](https://en.wikipedia.org/wiki/GNU_Compiler_Collection) is already preinstalled on [[Linux]] but if you don't have it (you must know what you're doing), here is the command (using *yay* as a AUR helper):
```shell
yay -Sy gcc-git
```

---

Here are some helpful commands :

To check your version of GCC :
```shell
g++ --version
```

To compile a single C++ file :
```shell
g++ [file]

#to run it just execute the binary
./a.out
```

To generate an executable :
```shell
g++ -o [bin] [file].cpp
```

The `-Wall` flag that shows *all* warning messages

To compile a static library:
```shell
#first compile to an object file
g++ -o [obj].o [file].cpp

#then use the `ar` utility with “rcs” to create an archive (“.a”) file
ar rcs [lib].a [obj].o

#to use this lib with g++
g++ -o [bin] [file].cpp [lib].a
```
---
## The preprocessor 

---
# Links
Here are the links to others obsidians notes (even if the appear before )
[[C++]] [[Linux]]