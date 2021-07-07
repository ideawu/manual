# docker 常用操作

### 仓库(repo)列表

```
docker images
```

### 实例(container, 虚拟机)列表

```
docker ps -a
```

### 新建实例(container)并第一次启动

```
docker run -it -v ~/host/dir:/root/share -p 127.0.0.1:22:22 --user root --workdir /root --hostname dev --name dev $repo bash
```

* `-v`: 挂载(共享)宿主机的目录
* `-p`: 将宿主机 127.0.0.1:22 映射到虚拟机的 22 端口, 这样, 只有本机能 ssh 访问
* `--hostname`: 虚拟机的主机名
* `--name`: 实例的名字, 不同实例不可重名
* `bash`: 启动虚拟机后, 执行 base, 不然虚拟机立即关机

### 启动实例

```
docker start -ai dev
```

### 保存实例到仓库

```
docker commit $container_name $repo:latest
```

### 备份实例(或者仓库))

```
docker export <container_id> -o dev.tar
docker export <repo:latest> -o dev.tar
```

### 导入实例(新建仓库, 或者覆盖仓库)

```
docker import dev.tar $repo:$tag
```

