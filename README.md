# A fork of Bellard QuickJS

## How to build
* 1. Windows
  
  Run in msys2.

```shell
/mingw64/bin/mingw32-make LDEXPORT="-static -s"
gcc -shared -o libquickjs.dll -static -s -Wl,--whole-archive libquickjs.a -lm -Wl,--no-whole-archive
```

* 2. MacOS
  