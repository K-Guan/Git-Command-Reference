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
    

``git commit -m '<commit text>'``
    将所有未提交的修改提交到当前分支

.. note::

    上面的 *#index* 意味着只会更改暂存区的内容，只有当commit之后才会生效。


|

--------
记录相关
--------

``git status``
    查看当前暂存区的状态

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

``git remote``
    管理/编辑/查看远程仓库

``git clone``
    从一个远程仓库“克隆”一个项目到本地

``git pull``
    获取在远程仓库上的某一分支的最新版本

``git push``
    向远程仓库推送当前分支的修改

``git push <branch name>``
    向远程仓库推送一个分支

``git push <tag name>``
    向远程仓库推送一个标签

|

--------
版本回退
--------

``git checkout -- <file>``
    撤销未在暂存区内文件<file>的修改

``git reset HEAD <file>``
    撤销位于暂存区内文件<file>的修改

``git reset HEAD``
    撤销所有暂存区内的修改

``git reset HEAD^``
    撤销最近一次提交的修改

.. note::
    
    git reset实际为版本回退命令，这个命令可以将您的文件回退到任意一个版本。

``git reset HEAD^^``
    回退到2个版本前

``git reset HEAD~5``
    回退到5个版本前

``git reset 2go8s97``
    回退到版本'2go8s97'

.. note::

    '2g08s97'是版本的SHA-1，您可以用git log来查看具体的SHA-1。
