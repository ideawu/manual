# 禁用命令不存在提示

影响速度, 必须卸载.

```
sudo apt remove command-not-found
```

# 禁用 ssh 登录提示, 太慢

```
cd /etc/update-motd.d
sudo chmod -x 10-help-text 50-landscape-sysinfo 50-motd-news 90-updates-available 91-release-upgrade
```
