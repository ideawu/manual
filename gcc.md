#### g++ 静态链接 libstdc++

```
g++ -static-libgcc -static-libstdc++ -l:`g++ -print-file-name=libstdc++.a` a.cpp
```

**必须指定 libstdc++.a 的路径!**

似乎是错的方法(如果使用的是旧版本的 g++ 或者用的是 gcc):

```
g++ -static-libstdc++ a.c
```


#### 指定链接某个库文件

```
gcc -l:/path/libxx.a
```

#### 运行时指定动态链接库的路径

```
LD_LIBRARY_PATH=/path/somewhere:$LD_LIBRARY_PATH my_program
```
