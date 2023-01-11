# Documentation

This program is a visualization/ simulation program designed to allow an interactive 3D environment. 

## Instructions 

Runs in Microsoft Visual studio. 

Be sure to set VC++ include and libs directory to usual settings.

Set additional libraries to usual settings and dependencies.

Set linker dependencies: assimp.lib, opengl32.lib, glfw3.lib along with usual dependencies.


![Screenshot 2023-01-11 180043](https://user-images.githubusercontent.com/110789514/211936610-3f1fb793-e384-46e2-b9de-c80d3ba3e4ba.png)

1. clone. Settings are MS Visual Studio x64. 

2. Modify solution properties, all solutions debug > VCC++.
add includes, add libraries

3. go to linker link additional libraries of config, dlls, bin, resources.
go to linker > input in properties add 
glfw3.lib, opengl32.lib, assimp.lib, freetype.lib

4. go to project add all existing items if missing items from below:
glad.c, stb_image.cpp, .pdbs, source, etc without duplicating source or adding solutions or other msvs files already detected. 

5. if filestystem.h warnings: 
after class FileSystem {
enter:
  public:
  #pragma warning(disable: 4996)

6. if using stb_image, add the following define below all includes: 
#define STB_IMAGE_IMPLEMENTATION
additional helpful macros:
#define STB_IMAGE_IMPLEMENTATION
#define STBI_ASSERT(x)
#define STBI_MALLOC
#define STBI_REALLOC 
#define STBI_FREE
#define STBI_NO_FAILURE_STRINGS
more info: see https://github.com/nothings/stb/blob/master/stb_image.h
if stb errors check for duplicate stb.cpp. 

7. using freetype, be sure to add freetype.lib, but also go to C++ language properties and add most recent c++ version to use the 2020 libraries. 

## License

Adobe Stock image by TenWit Standard License.
Credit to LearnOpenGL for camera, shaderss and glfw functions. 

https://github.com/JoeyDeVries/LearnOpenGL/blob/master/LICENSE.md

## References

Learn OpenGL, extensive tutorial resource for learning Modern OpenGL. (n.d.-c). https://learnopengl.com/
