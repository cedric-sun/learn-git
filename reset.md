在任何形式的reset命令中，省略`<tree-ish>`或`<commit>`都将默认使用HEAD

## Unstage a file
```
git reset -- <filename>
```

见`git help reset`的第一种形式

## Go Back to a previous Commit
```
git reset [<mode>] [<commit>]
```
见`git help reset`的第三种形式

**About mode:**
- mixed: reset index但是不改变working tree:
```
git reset --mixed [<commit>]
```
这将使所有自`<commit>`以来改动的文件变成unstage的状态
- hard: 抛弃`<commit>`之后的所有改动
```
git reset --hard [<commit>]
```
将回到`<commit>`刚完成时的状态，即stage area为空
- soft: 不改变index和working tree，只将HEAD恢复到`<commit>`
```
git reset --soft [<commit>]
```
这将使所有自`<commit>`以来改动的文件变成staged的状态
