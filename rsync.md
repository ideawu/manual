将本地文件夹同步到远端:

```
rsync -rzRv -e 'ssh -p 3927' $src user@1.2.3.4:~/dir/
```

从远端同步文件到本地, 不删除远端没有的文件:

```
rsync -rzv -e 'ssh -p 3927' user@1.2.3.4:~/dir/ $src
```

