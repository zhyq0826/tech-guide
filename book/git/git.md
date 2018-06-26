git 基本配置
=========

本文主要是对git 环境的基本配置

## git 的基本介绍

### 概述

git 是一个`版本控制系统(VCS)` 也就是一种记录一个或若干文件内容变化，以便将来查阅特定版本修订情况的系统. 

git 的[wiki](http://zh.wikipedia.org/wiki/Git)

### 在线文档

* [Pro Git](http://git-scm.com/doc) [中文版](http://git-scm.com/book/zh/v1)
* [Git Community Book](http://alx.github.io/gitbook/) [中文版](http://gitbook.liuhui998.com/)

## git 的使用

### 安装


**使包管理器安装**

```
$ sudo apt-get install git
```


**源码安装**

```sh

$ git clone https://github.com/git/git.git

$ cd git/

$ make prefix=/usr all

$ sudo make prefix=/usr install
```


### git 的基本设置


**设置你的称呼和邮箱**

```sh

$ git config --global user.name "YourName"

$ git config --global user.email "YourUserName@adesk.com"
```

**优化配置**

可以直接编辑`~/.gitconfig`文件进行配置. 样例如下:

```
[user]
    name = YourName
    email = YourUserName@adesk.com
[core]
    editour = vim
[merge]
    tool = vimdiff
[alias]
    co = checkout
    ci = commit -a
    st = status
    br = branch
    di = diff
    oneline  = log --pretty=oneline --since='2 days ago'
    onelog = log -p -1
[color]
    ui = auto
    interactive = auto
[color "branch"]
    current = yellow reverse
    local = yellow
    remote = green

[color "diff"]
    meta = yellow bold
    frag = magenta bold
    old = red bold
    new = green bold

[color "status"]
    added = green
    changed = magenta
    untracked = bold yellow
[diff]
    tool = vimdiff
```

### 实用工具

以下是两款较为方便的带图形化界面的git辅助工具,便于review代码

#### gitk

[主页](http://wiki.tcl.tk/14598)

[文档](http://git-scm.com/docs/gitk)

安装

```
$ sudo apt-get install gitk
```

#### gitg

[主页](https://github.com/jessevdk/gitg)

安装

```
$ sudo apt-get install gitg
```

