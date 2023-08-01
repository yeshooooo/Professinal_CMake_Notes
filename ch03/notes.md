# 1. Project()  
   每个CMake项目都应该包含一个 project() 命令，它应该在 cmake_minimum_required() 之后出现。该命令常见的
   选项如下所示:
```cmake
project(projectName
[VERSION major[.minor[.patch[.tweak]]]]
[LANGUAGES languageName ...]
)
```
  定义项目版本是一个好习惯，以便项目的其他部分可
以引用。第19章将深入讨论这个问题，并解释如何在CMakeLists.txt文件中引用版本信息。  
  LANGUAGES 参数定义了应该为项目启用的编程语言，支持的语言包括 C 、 CXX 、 Fortran 、 ASM 、 Java 等。
  如果指定了多种语言，请用空格分隔。某些情况下，项目可能不使用任何语言，这可以使用 NONE 。如果没有
  语言选项，CMake将默认为 C 和 CXX 。
  
