# glad

Files generated from [here](https://glad.dav1d.de) (Settings: C/C++, Spec: OpenGL, gl: Version 3.3, Profile: Corę).

## CMakeLists.txt
```
if (NOT TARGET glad)
    message(STATUS "Fetching glad")
    FetchContent_Declare(glad
        GIT_REPOSITORY https://github.com/Oceanic13/glad.git
        GIT_TAG "main"
        SOURCE_DIR "${EXTERNAL_DIR}/glad"
    )
    FetchContent_MakeAvailable(glad)
endif()

...

target_link_libraries(ProjectName
glad
...
)
```

## Include
```cpp
#include <glad/glad.h>
```