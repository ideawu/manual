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

# 安装 gcc-5 作为默认

```
sudo apt install g++-5
sudo apt install gcc-5

# Change the symlink to point to gcc 5 and g++ 5
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 10
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 20
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-5 10
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-5 20
sudo update-alternatives --install /usr/bin/cc cc /usr/bin/gcc 30
sudo update-alternatives --set cc /usr/bin/gcc
sudo update-alternatives --install /usr/bin/c++ c++ /usr/bin/g++ 30
sudo update-alternatives --set c++ /usr/bin/g++
```
