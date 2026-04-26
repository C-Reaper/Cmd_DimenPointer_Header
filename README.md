# Project README

## Overview
This project is a C application that demonstrates the use of a multi-dimensional data structure to store and print human names along with their IQ scores. The application supports different platforms including Linux, Windows (using Wine), WebAssembly, and cross-compilation for Windows on Linux.

## Features
- **Multi-Dimensional Data Structure**: The program uses a pointer to an array of pointers, each representing a 2D array that stores `Human` structures.
- **Dynamic Memory Allocation**: Memory is dynamically allocated for the multi-dimensional structure.
- **Memory Management**: Proper memory allocation and deallocation using `malloc`, `calloc`, and `free`.
- **Custom Data Structure**: A custom `Human` structure to store each individual's name, IQ score, and dimensions.

## Project Structure
```
Project/
├── build/              # .exe files produced by Main.c
├── src/
│   ├── Main.c          # Entry point
│   └── *.h             # stand alone Header-based C-files, without *.c files that implement it
├── Makefile.linux      # Linux Build configuration
├── Makefile.windows    # Windows Build configuration
├── Makefile.wine       # Wine Build configuration
└── README.md           # This file
```

### Prerequisites
- **C/C++ Compiler and Debugger**: GCC, Clang, or any C compiler that supports the specified flags.
- **Make Utility**: For building the project.
- **Standard Development Tools**: Required for setting up the development environment.

## Build & Run
### Linux
To build and run on Linux:
```sh
cd Project/
make -f Makefile.linux all
make -f Makefile.linux exe
```

### Windows (using Wine)
To build and run on Windows using Wine:
```sh
cd Project/
make -f Makefile.wine all
make -f Makefile.wine exe
```

### WebAssembly
To build and run the project for WebAssembly:
```sh
cd Project/
make -f Makefile.web all
make -f Makefile.web exe
```

### Windows (cross-compilation on Linux)
To build a Windows executable on Linux using Wine:
```sh
cd Project/
make -f Makefile.wine clean
make -f Makefile.wine all
make -f Makefile.wine exe
```

This project provides a clear and concise example of how to handle multi-dimensional data structures, manage memory, and utilize different build environments.