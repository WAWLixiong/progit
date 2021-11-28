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

# log

1. `git log -p -2`
    1. 显示path信息,即代码信息, -2显示最近2次提交
2. `git log --stat`
    1. 显示统计信息
3. `git log --pretty=oneline`
    1. 展示不同形式的提交信息, 还有 `short`, `full`, `fuller`, `format`
    2. `format`的选项
4. `git log --pretty=oneline --graph`
5. `git log -S <function_name`
    1. 只查询增加或删除了该字符串的提交
    2. -S 俗称 pickaxe 用鹤觜锄在土里捡石头
6. `git log -- <path>`
    1. 只查询特定目录的历史提交

# 撤销操作

1. `git commit --amend`
    1. 命令会将暂存区中的文件提交
    2. 修改commit信息
2. `git reset HEAD <file>`
    1. untracked单个文件
3. `git checkout -- <file>`
    1. 撤销之前的文件修改(更合理的工作流是创建分支进行工作)

# 远程仓库

1. `git remote -v`
    1. 展示需要读写远程仓库的简称与URL
2. `git remote add <shortname> <url>`
    1. 添加一个新的远程git仓库
3. `git push <remote> <branch>`
    1. 推送到远程仓库
4. `git remote show origin`
    1. 列出在特定分支上执行`git push`会自动推送到哪一个远程分支
5. `git remote rename <old> <new>`
    1. 远程仓库重命名 
6. `git remote rm <origin>`
   1. 移除远程仓库

# 打标签
1. `git tag -l` 或 `git tag -l "v1.8.5*"`
   1. 按字母顺序列出标签
2. 轻量标签(lightweight)
   1. 像一个不会改变的分支, 只是某个特定提交的引用
3. 附注标签(annotated)
   1. git数据库中的一个完整对象, 它们是可以被校验的
   2. 对象中包含打标签者的名字,电子邮件,日期时间等信息, 通常建议打附注标签
