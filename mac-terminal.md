# 避免 Mac Terminal 终端和 SSH 显示 UTF-8 错误信息

首先, Terminal 的高级选项 "Set locale environment variables on startup" 必须选中, 否则无法正常显示中文. 接着, 用 Terminal SSH 某些服务器, 会在服务器上提示错误信息:

```
warning: setlocale: LC_CTYPE: cannot change locale (UTF-8)
```

这时, 你需要修改你的 Mac 机器上的 `~/.bash_profile`, 加上

```
export LC_ALL="en_US.UTF-8"
export LC_CTYPE="en_US.UTF-8"
```

# 使用 bash, 不使用 zsh

```
chsh -s /bin/bash
```

# 影藏 Terminal 启动时的显示信息

修改 `~/.bash_profile`

```
export BASH_SILENCE_DEPRECATION_WARNING=1
```

# 避免滚屏变成箭头键

当你运行 vim 之后, 鼠标或者触板滚屏时, 并没有滚屏, 而是变成了按上下箭头. 修改 Terminal.app 的 Preferences->Profiles->Keyboard, 取消 Scroll alternate screen.
