## Working tree and Index
```
git diff [--options] [--] [<file>...]
```

## Index and a specific commit
```
git diff [--options] --cached [<commit>] [--] [<file>...]
```

If `[<commit>]` is omitted, HEAD is used.

`--staged` is a synonym of `--cached`.

## Working tree and a specific commit
```
git diff [--options] <commit> [--] [<file>..]
```
**e.g.** Diff current working tree and HEAD:
```
git diff HEAD
```

## Just normally diff 2 files on filesystem
```
git diff --no-index [--options] [--] [<file>...]
```
