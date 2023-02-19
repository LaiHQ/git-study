
# 提交--------------------------
## 当前目录下所有的文件提交到暂存区 
git add .

## 指定文件提交到暂存区
git add 1.txt

## 取消暂存区提交
git restore HEAD 1.txt(文件名)

or

git restore --staged 1.txt


## 取消提交的commit
git reset --hard head


# 查看--------------------------
查看提交所在区域状态 git status 
查看仓库源 git remote -v

查看远程分支更新 get fetch


--------------------------



# tag--------------------------
## 添加
git tag v1.0.0

## 列举
git tag --list

## 推送
git push origin main --tags


## 删除
本地：git tag -d tag名称
远程：git push origin :refs/tags/tag名称




# 分支--------------------------

以当前分支复制一份到新创建的分支：git branch dev

以当前分支复制一份且切换到新创建的分支：git checkout  -b dev


## 删除
本地 git branch -D 分支名称
远程 git push origin :分支名称


# 拉取--------------------------
拉取指定分支：git pull origin dev

只拉取远程的更新，不会把远程更新到本地来: git fetch origin dev
他会将远程更新到一个 FETCH_HEAD 里面 之后 git merge FETCH_HEAD

git fetch 一般用于合并某一个分支的内容

比如将dev的内容合并到test分支去  `git fetch origin dev:test`


查看远程分支是否有更新 get fetch

如果有拉去过来 `git fetch origin 来源分支:本地分支`

将dev分支合并到当前分支 `get merge dev`


git fetch + git merge  等同于git pull


# 推送--------------------------
推送到指定分支: git push origin main 

将本地feature分支推送到远程dev分支：`git push origin feature:dev`


删除缓存 `git rm --cached -r . ` 并不会删除提交日志和快照


## 恢复删除

# 合并


