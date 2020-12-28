# 禁用命令不存在提示

影响速度, 必须卸载.

```
sudo apt remove command-not-found
```

# 禁用 ssh 登录提示, 太慢

```
sudo chmod -x /etc/update-motd.d/50-landscape-sysinfo /etc/update-motd.d/50-motd-news /etc/update-motd.d/90-updates-available
```
