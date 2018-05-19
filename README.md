# NanoVG Haskell bindings

[![Build Status](https://img.shields.io/travis/cocreature/nanovg-hs.svg)]()
[![Hackage](https://img.shields.io/hackage/v/nanovg.svg)]()

Currently only the GL3 backend is supported.

A large part of the example bundled with
[NanoVG](https://github.com/memononen/nanovg) is translated into
Haskell and bundled as `example00`.

Most of the bindings directly expose the corresponding
[NanoVG](https://github.com/memononen/nanovg) so look there for more
details on the usage.

There is also a [diagrams backend](https://github.com/cocreature/diagrams-nanovg) using these bindings.

Feel free to open issues if you have any ideas for improvements (or even better PRs :)).

### Building on Windows

#### Update Stack's embedded msys

```stack exec -- pacman -Syu```

#### Install required dependencies

```stack exec -- pacman -S mingw-w64-x86_64-pkg-config mingw-w64-x86_64-freeglut mingw-w64-x86_64-glew```

#### Copy .dlls to your project

This step should no be necessary, and you can actually put msys' path in your PATH, but whenever you upgrade to a newer GHC you will be forced to update it.

Copy ```glew32.dll``` from

```C:\Users\<username>\AppData\Local\Programs\stack\x86_64-windows\msys2-20150512\mingw64\bin```

to the root of your project.
