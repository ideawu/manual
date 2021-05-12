# SSH 免密登录

在工作机执行:

```
ssh-keygen -t rsa
```

在服务器新建 `~/.authorized_keys`, 内容就是工作机的 `.ssh/id_rsa.pub ` 文件内容.

```
chmod uo-rwx ~/.authorized_keys
```

远程执行命令

```
ssh user@ip -p 21 "ls"
```
