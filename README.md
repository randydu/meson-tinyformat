# meson-tinyformat

Meson subproject wrap for tinyformat

URLs: 

- [github: tinyformat.h](https://github.com/c42f/tinyformat.git);
- [github: meson-tinyformat](https://github.com/randydu/meson-tinyformat.git);

The subfolder "src" is a clone of git repository of a specified tinyformat release version. 

## Versions

The "revision" of gsl.wrap and the version of this meson-build project matches the embedded submodule GSL version as following:

meson-tinyformat |  tinyformat 
-----------------|-----------
v1.0              | v2.3.0


## Usage

copy tinyformat.wrap from this project to the "subprojects" sub-folder of your project directory.


in meson.build:

```
# import

tfm_dep = dependency('tinyformat')

# use
srcs = ['main.c', ...]

executable('test', srcs, dependencies: [tfm_dep, ...])

```

in main.c:

```c
#include <tinyformat.h>

void foo(int x){
    tfm::printfln("Hello World");
}
```



