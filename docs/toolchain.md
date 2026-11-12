# Toolchain

Primary environment: Debian via WSL or Linux, VS Code, Git, GCC/Clang, GDB,
CMake when a project needs a build system.

Check what is installed:

```bash
git --version
g++ --version
clang++ --version
cmake --version
gdb --version
```

Some commands may be missing initially. Verify C++23 feature support rather than
assuming every compiler and standard library implements it completely.

For a simple single-file exercise, an example development build is:

```bash
mkdir -p build
g++ -std=c++23 -Wall -Wextra -Wpedantic -g practice/example/main.cpp -o build/example
./build/example
```

The path `practice/example/main.cpp` is illustrative; create it only when needed.
For multi-file projects, introduce CMake and tests as appropriate.
