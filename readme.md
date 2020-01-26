![Cover Art](https://alain.xyz/blog/raw-opengl/assets/cover.jpg)

# ⚪ OpenGL Seed WebAssembly

[![CMake][cmake-img]][cmake-url]
[![License][license-img]][license-url]

- [🐟 Glitch Example](https://glitch.com/~opengl-seed-wasm)

- [💬 Blog Post](https://alain.xyz/blog/raw-opengl)

An example build of the [OpenGL Seed](https://github.com/alaingalvan/opengl-seed) built for WebAssembly.

## Setup

First install:

- [Git](https://git-scm.com/)

- [CMake](https://cmake.org)

- A Text Editor such as [Visual Studio Code](https://code.visualstudio.com/).

- [Emscripten SDK](https://kripken.github.io/emscripten-site/docs/getting_started/downloads.html), make sure to add it's Emscripten installation to your `PATH`.

Then type the following in any terminal your such as [VS Code's Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal).


> **Note**: if you're on Windows, I would highly recommend using the [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).

```bash
# 🐑 Clone the repo
git clone https://github.com/alaingalvan/opengl-seed --recurse-submodules

# 💿 go inside the folder
cd opengl-seed

# 👯 If you forget to `recurse-submodules` you can always run:
git submodule update --init

# ⚠️ Possible dependencies you might need:
sudo apt-get update
sudo apt-get install cmake build-essential llvm

# 👷 Make a build folder
mkdir wasm
cd wasm

# 🔨 Build the project
emcmake cmake ..
emmake make OpenGLSeed -j
```

From there create an HTML file that loads the generated `OpenGLSeed.js` file, and run an http server.

[cmake-img]: https://img.shields.io/badge/cmake-3.6-1f9948.svg?style=flat-square
[cmake-url]: https://cmake.org/
[license-img]: http://img.shields.io/:license-unlicense-blue.svg?style=flat-square
[license-url]: http://unlicense.org/