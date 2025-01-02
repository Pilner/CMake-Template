<h1 style="text-align: center">CMake Basic Template</h1>

<p style="text-align: center">To quickly setup a C/C++ Project using CMake</p>

## How to use

_Note: Make sure you have [CMake](https://cmake.org/download/) installed. To check, run `cmake --version` in your terminal_

1. Click `Use this template` or clone into a local directory

```bash
git clone https://github.com/Pilner/CMake-Template.git
```

2. Setup `CMakeLists.txt` to your liking

```C
# Minimum CMake version required
cmake_minimum_required(VERSION 3.10)

# Project name and language
project(PROJECT_NAME) // Change PROJECT_NAME

# Specify C standard
set(CMAKE_C_STANDARD 11)
set(CMAKE_C_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Add include directories
include_directories(include)

# You can also include external libraries, e.g. SDL2

# Add source files
file(GLOB SOURCES "src/*.c")

# Add the executable
add_executable(PROJECT_NAME ${SOURCES}) // Change PROJECT_NAME

```

3. Once in the root directory of the repository, create a `build/` folder

```bash
mkdir build
cd build
```

4. Compile CMake using the `CMakeLists.txt`

```bash
# pwd is ../build
cmake ..
```

5. Build the CMake to Link the Libraries and Generate Executable

```bash
# pwd is ../build
cmake --build .
```

6. Execute the Generated Executable

```bash
# pwd is ../build
./PROJECT_NAME
```

7. In order to rebuild, delete `build/` and recreate steps **3 - 5**

```bash
rm -rf build
mkdir build
cd build
cmake ..
cmake --build .
```
