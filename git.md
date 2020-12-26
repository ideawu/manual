# Git 常用操作

### 避免 git pull 自动 merge

Why the FUCK!

```
git pull --rebase
```

### 用 master 覆盖分支(sync branch exactly with master)

```
git fetch origin
git reset --hard origin/master
git commit --force
```

### 忽略本地修改(未 commit 到远程)

```
git reset --hard HEAD
git reset --hard commit_id
```

### 修改 commit 历史

```
git rebase -i 0ad14fa5(想修改此条之后的记录, 不包括此条)
# 然后针对要修改的记录, 改为 edit
# 接着修改
git commit --amend --author="www <abc@www.org>" --no-edit
git push -f
```
