# A fork of Bellard QuickJS

## How to build
* 1. Windows
  
  Run in msys2.

```shell
/mingw64/bin/mingw32-make LDEXPORT="-static -s"
gcc -shared -o libquickjs.dll -static -s -Wl,--whole-archive libquickjs.a -lm -Wl,--no-whole-archive
```
  test.

```shell
./qjsc.exe -e -o hello.c examples/hello.js
gcc -D_GNU_SOURCE -I./ -o hello hello.c -static -s -L./ -lquickjs -lm -ldl -lpthread
./hello
```

* 2. MacOS
  