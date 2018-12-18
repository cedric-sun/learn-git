曾经困惑过当需要unstage一个index中的change的时候，`git reset`和`git rm --cached`有什么区别

事实上`git rm --cached`根本不是用来unstage change的，这条命令会只在index中将该文件标记为删除，这样该文件就会变为untracked，下次commit的时候该文件就会从HEAD中消失

尽管如此，如果`git rm --cached`一个从未commit过的文件，效果就是该文件被unstage了一样，因此这两条命令容易混淆

Reference: https://stackoverflow.com/questions/6919121/why-are-there-2-ways-to-unstage-a-file-in-git
