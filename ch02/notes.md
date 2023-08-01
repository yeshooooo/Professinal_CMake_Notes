* 一些生成器支持多种配置,可以在不同的配置中进行选择，不必重新运行cmake
如：Visual Studio 和 XCode  
* 不支持多种配置的生成器。必须重新运行Cmake在Debug和Release等之间进行切换构建方式。
* 对于多个配置， --config 选项指定要构建哪个配置，而单个配置生成器将忽略 --config 选项，而依赖于执行CMake项目生成时
  的信息。13章将详细介绍构建配置。
* --target 选项可以用来告诉构建工具要构建什么目标，如果省略该选项，将构建默认目标。
```shell
cmake --build /some/path/build --config Debug --target MyApp
```
* Ninja生成器是后者最佳的选择，因为它支持的平台最广泛，还能进行非常高效的构建
* cmake --build 调用构建工具，而非直接调用构建工具。