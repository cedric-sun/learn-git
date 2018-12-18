git rm用来将文件从index和working tree上同时删除

删除的文件必须在working tree和index上保持一致，即index中不能有任何对该文件的修改(除非加上-f 或 --cached)

## Delete only from index
```
git rm --cached -- <file>
```

不会影响文件系统上的该文件，因此index将该文件标记为已删除之后，该文件的状态为untracked
