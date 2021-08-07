## The test of git

## Git 分支机制
    1.Git采用一系列快照的方式存储数据，当发起提交时，Git存储的是提交对象(commit object)
      提交对象包括作者姓名和邮箱地址等信息以及指向其父提交的指针
    2.Git的分支是一个指向某次提交的轻量级的可移动指针(movable pointer)。
      Git默认的分支名为master，当发起提交时，就有了一个指向最后一次提交的master分支，每次提交时，都会自动向前移动。
    注：在Git中，master分支其实并不是特殊的分支，与其他分支没有区别，几乎每个Git仓库都拥有该分支，因为git init会默认创建该分支。

    创建新分支
        git branch testing
    创建新分支的同时会创建一个指向当前提交的新指针

    原理：Git如何知道当前处在哪个分支上呢？

    实际上Git维护着一个名为HEAD的特殊指针，这是一个指向当前所在的本地分支的指针

    可以通过 git log 查看各个分支当前所指向的对象 ，需要用到 --decorate 选项

    git log --oneline --decorate

    切换分支
    git checkout testing
