## Overview
The project appears to be a simple C-based application that displays a triangle on the screen and allows users to interact with it. The application includes basic features such as drawing the triangle, detecting mouse clicks within the triangle, and changing color based on whether the click is inside or outside the triangle.

## Features
- Drawing a triangle on the screen.
- Detecting mouse clicks within the triangle.
- Changing color of the triangle based on whether the click is inside or outside.

## Project Structure
- `src/Main.c` - The entry point of the application, which includes the main function and handles window setup, rendering, and user input.
- `src/*.h` - Header files used by `Main.c`, but no `.c` files are provided in the tree.

### Prerequisites
- C/C++ Compiler (GCC)
- Make utility
- Standard development tools
- X11 library for Linux or a compatible windowing system for other platforms

## Build & Run
To build and run the application, follow these steps:

### Building
```sh
# For Linux
make -f Makefile.linux all

# For Windows
make -f Makefile.windows all

# For Wine (Linux cross compile for Windows)
make -f Makefile.wine all

# For WebAssembly (Emscripten or wasmtime)
make -f Makefile.web all
```

### Cleaning and Rebuilding
```sh
# Clean and rebuild for Linux
make -f Makefile.linux clean
make -f Makefile.linux all

# Clean and rebuild for Windows
make -f Makefile.windows clean
make -f Makefile.windows all

# Clean and rebuild for Wine (Linux cross compile for Windows)
make -f Makefile.wine clean
make -f Makefile.wine all

# Clean and rebuild for WebAssembly (Emscripten or wasmtime)
make -f Makefile.web clean
make -f Makefile.web all
```

### Running
```sh
# Run the application for Linux
make -f Makefile.linux exe

# Run the application for Windows
make -f Makefile.windows exe

# Run the application for Wine (Linux cross compile for Windows)
make -f Makefile.wine exe

# Run the WebAssembly application in a browser
make -f Makefile.web exe
```

The project includes four different makefiles tailored to different platforms and build environments:
- `Makefile.linux` for building on Linux.
- `Makefile.windows` for building on Windows using MinGW or MSYS2.
- `Makefile.wine` for building on Linux with the intention of running the application under Wine.
- `Makefile.web` for building a WebAssembly version that can be run in any browser.

Each makefile is designed to compile and link the necessary source files into an executable binary that is platform-specific.