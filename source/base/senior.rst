========
高级命令
========

|

``git stash``
    储藏index内的所有未提交的修改
    
.. note::
    
    您可以将暂时不想提交的文件储藏起来去修改并提交其他的文件。还原请用：git stash pop。

``git archive <branch>``
    将一个分支打包为压缩文件

.. warning::

    请添加-o <file>参数则输出到文件，不然将会直接将压缩后文件的内容打印到屏幕。


``git blame <file>``
    查看文件每一行的编辑者与编辑时间

``git cherry <branch>``
    查看分支<branch>与当前分支的区别

``git difftool <file1> <file2>``
    使用外部diff程序(如vimdiff)来查看代替diff

``git bisect``
    记录从运行到结束之间的所有变更，一般为调试用

``git commit --amend -m <new text>``
    修改您最近一次commit时提交的文本介绍

``git revert HEAD``
    反转一次操作

.. note::
    
    比方您删除了file，那么反转后等于重新添加了。您也可以随意更改HEAD为任意一次commit。

