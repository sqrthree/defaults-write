[English](./README.md) · [简体中文](./README-zh.md)

# defaults-write

这些隐藏的命令会让你的 Mac 更好用。

> 你不需要知道每一件事，只需要知道在哪里可以找到它。 —— 爱因斯坦

## 导航

- [在 Dock 左侧添加空白符以更好的组织应用（应用区）](#在-dock-左侧添加空白符以更好的组织应用应用区)
- [在 Dock 左侧添加“紧凑的”空白符以更好的组织应用（应用区）](#在-dock-左侧添加紧凑的空白符以更好的组织应用应用区)
- [在 Dock 右侧添加空白符以更好的组织应用（废纸篓区）](#在-dock-右侧添加空白符以更好的组织应用废纸篓区)
- [在 Dock 右侧添加“紧凑的”空白符以更好的组织应用（废纸篓区）](#在-dock-右侧添加紧凑的空白符以更好的组织应用废纸篓区)
- [取消自动隐藏 Dock 的触发时间](#取消自动隐藏-dock-的触发时间)
- [加快 Mission Control 的动画效果](#加快-mission-control-的动画效果)
- [重置为默认的 Mission Control 的动画速度](#重置为默认的-mission-control-的动画速度)
- [让 Dock 中隐藏的程序图标半透明](#让-dock-中隐藏的程序图标半透明)
- [拷贝 Mail.app 中的邮件地址时不使用全名](#拷贝-mailapp-中的邮件地址时不使用全名)
- [在“快速查看”中开启文本选择功能](#在快速查看中开启文本选择功能)
- [禁用“你确定要打开这个应用吗？”对话框](#禁用你确定要打开这个应用吗对话框)
- [为 Dock 栏中的正在运行的应用添加指示灯](#为-dock-栏中的正在运行的应用添加指示灯)
- [在 Finder 中显示状态栏](#在-finder-中显示状态栏)
- [默认开启使用安全模式清空垃圾篓](#默认开启使用安全模式清空垃圾篓)
- [保存文件时默认显示文件夹目录列表](#保存文件时默认显示文件夹目录列表)
- [自定义截图保存的位置](#自定义截图保存的位置)
- [关闭窗口和菜单的透明度](#关闭窗口和菜单的透明度)
- [显示调试按钮](#显示调试按钮)
- [隐藏“桌面”图标](#隐藏桌面图标)
- [在 Finder 中始终显示隐藏的文件和文件夹](#在-finder-中始终显示隐藏的文件和文件夹)
- [调整启动台中的行数](#调整启动台中的行数)
- [调整启动台中的列数](#调整启动台中的列数)
- [重置启动台的布局为默认状态](#重置启动台的布局为默认状态)
- [在 Finder 中显示路径导航条](#在-finder-中显示路径导航条)
- [设置“当前文件夹”为默认的搜索区域](#设置当前文件夹为默认的搜索区域)
- [只让菜单栏和 Dock 栏变为深色模式](#只让菜单栏和-dock-栏变为深色模式)

### 在 Dock 左侧添加空白符以更好的组织应用（应用区）

```bash
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 在 Dock 左侧添加“紧凑的”空白符以更好的组织应用（应用区）

```bash
defaults write com.apple.dock persistent-apps -array-add '{tile-data={}; tile-type="small-spacer-tile";}' && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 在 Dock 右侧添加空白符以更好的组织应用（废纸篓区）

```bash
defaults write com.apple.dock persistent-others -array-add '{tile-data={}; tile-type="spacer-tile";}' && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 在 Dock 右侧添加“紧凑的”空白符以更好的组织应用（废纸篓区）

```bash
defaults write com.apple.dock persistent-others -array-add '{tile-data={}; tile-type="small-spacer-tile";}' && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 取消自动隐藏 Dock 的触发时间

```bash
defaults write com.apple.Dock autohide-delay -float 0 && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 加快 Mission Control 的动画效果

```bash
// you can adjust the animation speeds by changing the number after the -float flag。
defaults write com.apple.dock expose-animation-duration -float 0.15 && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 重置为默认的 Mission Control 的动画速度

```bash
defaults delete com.apple.dock expose-animation-duration && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 让 Dock 中隐藏的程序图标半透明

```bash
defaults write com.apple.dock showhidden -bool YES && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 拷贝 Mail.app 中的邮件地址时不使用全名

```bash
defaults write com.apple.mail AddressesIncludeNameOnPasteboard -bool false
```

[⬆️ 返回顶部](#defaults-write)

### 在“快速查看”中开启文本选择功能

```bash
defaults write com.apple.finder QLEnableTextSelection -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 禁用“你确定要打开这个应用吗？”对话框

```bash
defaults write com.apple.LaunchServices LSQuarantine -bool false
```

[⬆️ 返回顶部](#defaults-write)

### 为 Dock 栏中的正在运行的应用添加指示灯

```bash
defaults write com.apple.dock show-process-indicators -bool true && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 在 Finder 中显示状态栏

```bash
defaults write com.apple.finder ShowStatusBar -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 默认开启使用安全模式清空垃圾篓

```bash
defaults write com.apple.finder EmptyTrashSecurely -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 保存文件时默认显示文件夹目录列表

```bash
defaults write -g NSNavPanelExpandedStateForSaveMode -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 自定义截图保存的位置

```bash
defaults write com.apple.screencapture location -string "$HOME/Desktop"
```

[⬆️ 返回顶部](#defaults-write)

### 关闭窗口和菜单的透明度

```
defaults write com.apple.universalaccess reduceTransparency -bool true
```

[⬆️ 返回顶部](#defaults-write)

### 显示调试按钮

```
defaults write com.apple.appstore ShowDebugMenu -bool true
```

[⬆️ 返回顶部](#defaults-write)

### 隐藏“桌面”图标

```bash
defaults write com.apple.finder CreateDesktop -bool false && killall Finder
```
[⬆️ 返回顶部](#defaults-write)

### 在 Finder 中始终显示隐藏的文件和文件夹

```
defaults write com.apple.finder AppleShowAllFiles -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 调整启动台中的行数

```
defaults write com.apple.dock springboard-rows -int 6 && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 调整启动台中的列数

```
defaults write com.apple.dock springboard-columns -int 8 && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 重置启动台的布局为默认状态

```
defaults write com.apple.dock ResetLaunchPad -bool true && killall Dock
```

[⬆️ 返回顶部](#defaults-write)

### 在 Finder 中显示路径导航条

```bash
defaults write com.apple.finder ShowPathbar -bool true && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 设置“当前文件夹”为默认的搜索区域

```bash
defaults write com.apple.finder FXDefaultSearchScope -string "SCcf" && killall Finder
```

[⬆️ 返回顶部](#defaults-write)

### 只让菜单栏和 Dock 栏变为深色模式

```bash
defaults write -g NSRequiresAquaSystemAppearance -bool Yes
```

[⬆️ 返回顶部](#defaults-write)
