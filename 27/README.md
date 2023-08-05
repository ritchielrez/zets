# Cmake project options

If you are using any other people's library, which uses `cmake`, and also including the library to your own `cmake` project,
then make sure check the librarie's `CMakeLists.txt` for options. Options that you can turn on or off, like suppose you want
to link the library with static linking, there should be an option. This is crucial, for libraries like `SDL2`, to make sure
you are telling the library to build static library, if you want to properly link to the project.

Suppose a scenario, where you decided to put this following line of code in your `CMakeLists.txt`:
```
target_link_libraries(${PROJECT_NAME} PRIVATE SDL2_image::SDL2_image-static)
```
Here, we are linking our project to the `SDL_image` target, which is only built when you specify you want to build staic version
of the library, though turning on the `BUILD_SHARED_LIBS` option like this:
```
option(BUILD_SHARED_LIBS "Build the library as a shared library" OFF)
```
Many projects will respect this option, and build a static library if you include them in your project.
