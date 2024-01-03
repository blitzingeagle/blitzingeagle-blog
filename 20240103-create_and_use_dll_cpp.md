# Create and Use DLL in C++

2024-01-03

## What is a DLL

DLL stands for Dynamic Link Library. It is a file that contains compiled code that can be dynamically linked at runtime to be used by multiple programs simultaneously. This is a contrast to static libraries which are integrated directly in the executable during compile-time.

In Unix-like systems (including Linux), DLLs are referred to as Shared Objects (SO). While Windows uses the `.dll` extension for DLLs, Unix uses `.so` for SOs.

## Creating DLL in C++

### Directory Structure

To create a DLL with C++, structure your C++ project similar to this example.

```
project/
|-- src/
|   |-- example.cpp
|-- include/
|   |-- example.h
|-- CMakeLists.txt
```



