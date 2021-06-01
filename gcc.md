#### g++ 静态链接 libstdc++

```
g++ -static-libgcc -l:`g++ -print-file-name=libstdc++.a` a.cpp
```

似乎是错的方法:

```
g++ -static-libstdc++ a.c
```


#### 指定链接某个文件

```
gcc -l:/path/libxx.a
```
