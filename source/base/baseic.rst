========
常用命令
========

|

--------
基础操作
--------

``git init``
    将当前目录初始化为一个git仓库

``git add <file>``
    向分支添加一个(或多个)文件   *#index*
 
``git rm <file>``
    从分支移除一个(或多个)文件   *#index*

``git mv <file1> <file2>``
    移动或重命名分支的一个文件   *#index*

.. note::

    如果使用mv而不是git mv的话，需要手动git rm之前的文件并git add新文件。
    

``git commit``
    将所有未提交的修改提交到当前分支

.. note::

    上面的 *#index* 就是意味着只会更改暂存区的内容，只有当commit之后才会生效。


|

--------
记录相关
--------

``git status``
    查看当前index的状态

``git log``
    查看全部的提交记录

``git show``
    查看提交记录的详细信息

``git diff <version1> <version2>``
    比较两个版本之间的差异

|

--------
分支相关
--------

``git branch``
    查看现有的分支

``git branch <name>``
    创建一个新分支

``git branch -d <name>``
    删除一个新分支

``git checkout <name>``
    切换到另一个分支

``git checkout -b <name>``
    创建并切换到一个分支

``git merge <name>``
    将分支<name>合并到当前分支

|

--------
标签相关
--------

``git tag``
    查看现有的标签

``git tag <name>``
    创建一个标签

``git tag -d <name>``
    删除一个标签

``git tag <name> f3g7437``
    为版本号'f3g7437'创建一个标签

``git show <name>``
    查看一个标签的详细信息

|

--------
远程相关
--------

``git clone``
    从一个远程服务器“克隆”一个项目到本地

``git pull``
    获取在远程服务器上的某一分支的最新版本

``git push``
    向远程服务器推送当前分支的修改

``git push <branch name>``
    向远程服务器推送一个分支

``git push <tag name>``
    向远程服务器推送一个标签

|

--------
版本回退
--------

``git checkout -- <file>``
    撤销一次普通的修改(更改一个文件，但是没有git add)
    
``git reset HEAD``
    撤销一次index修改(已经git add的文件，或git rm/mv的文件)

``git reset HEAD^``
    撤销已经提交的修改(已经commit的修改)

.. note::
    
    实际上git reset是一个版本回退的命令，这个命令是回退到上一个版本，见下文。

``git reset HEAD^^``
    回退到2个版本前

``git reset HEAD~5``
    回退到5个版本前

``git reset 2g08s97``
    回退到版本'2g08s97'

.. note::

    '2g08s97'是版本号，您可以用git log来查看具体的版本号。
