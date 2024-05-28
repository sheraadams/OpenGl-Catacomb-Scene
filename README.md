# OpenGL Catacombs Scene

## About the Project

This program is a visualization/ simulation program designed to allow an interactive 3D environment. 

Watch the youtube video here: 
https://www.youtube.com/watch?v=ATzwJx1fmJM

## Instructions 

Runs in Microsoft Visual studio. 

Be sure to set VC++ include and libs directory to usual settings.

Set additional libraries to usual settings and dependencies.

Set linker dependencies: assimp.lib, opengl32.lib, glfw3.lib along with usual dependencies.


![Screenshot 2023-01-11 180043](https://user-images.githubusercontent.com/110789514/211936610-3f1fb793-e384-46e2-b9de-c80d3ba3e4ba.png)

1. Clone. Settings are MS Visual Studio x64. 

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
and other macros can be found here: see https://github.com/nothings/stb/blob/master/stb_image.h 


## References

DeVries, J. (n.d.). LearnOpenGL/LICENSE.md at master · JoeyDeVries/LearnOpenGL. GitHub. https://github.com/JoeyDeVries/LearnOpenGL/blob/master/LICENSE.md

Learn OpenGL, extensive tutorial resource for learning Modern OpenGL. (n.d.-d). https://learnopengl.com/

TenWit. (n.d.). Ancient Egyptian hieroglyphics carved on a stone wall. https://as1.ftcdn.net/v2/jpg/03/98/12/30/1000_F_398123053_OTZVcEOx2NmitYsU4Gac13ZsX7scfVPt.jpg
