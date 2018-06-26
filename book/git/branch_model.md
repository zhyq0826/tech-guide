git 分支模型
================

![git分支模型图](http://s.androidesk.com/docs/git%E5%88%86%E6%94%AF%E6%A8%A1%E5%9E%8B.gif)

### 基本介绍

日常维护分支为`dev`和`master`分支, `master`分支为线上运行的稳定分支, `dev`分支是开发分支.日常开发任务如果是新功能需从`dev`切出新分支进行开发(分支命名`feature-*`),开发并测试得到稳定代码后合并至`dev`,再切出稳定分支(分支命名`release-*`)用以上线. 详细说明看如下文档.

### 分支命名规则
 

```sh

feature-*    //特性分支

release-*    //发布分支

hotfix-*     //快速修复分支 (从master 中切出)

```

### 文档

[英文原版](http://nvie.com/posts/a-successful-git-branching-model/)

[中文翻译](http://blog.csdn.net/dbzhang800/article/details/6798724)
