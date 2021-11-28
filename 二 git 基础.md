# 状态简览
1. `git status -s`
   1. |符号|含义|
      |---|---|
      |??|untracked|
      |A|新加到暂存区|
      |M|修改过的文件|
      |MM|左侧表示暂存区的状态,右侧表示工作区的状态|

# diff
1. `git diff`
   1. 比较未暂存的文件与已暂存文件的差异
2. `git diff --staged` 或 `git diff --cached`
   1. 比较已暂存文件与最后一次commit的文件差异

# add

# commit
1. `git commit -a -m "<msg>"` 
   1. add + commit

# rm
1. `git rm <file>`
   1. 将文件删除, 并做了add操作
2. `gir rm --cached <file>`
   1. 将文件从暂存区移到工作区, 即untracked