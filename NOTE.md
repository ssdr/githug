> 通过前41关啦！

# 关于Git的一点笔记

#### 配置
    git config --global user.name Damian
    git config --global user.email ssdr_liu@163.com
    
#### 删除git管理的文件，不在文件系统删除
    git rm --cached file
    
#### 暂存文件
    git stash
    git stash list
    git stash apply
    
#### tag
    git tag -l
    git tag new_tag
    git tag -d new_tag
    
#### push
    git push origin tag_to_be_pushed 推送特定tag到远端
    git push --tags 推送所有tags到远端
    
#### 指定提交的日期时间
    git commit --date "Thu Dec 31 13:34:03 2016 +0800" -m "xxx"

#### 恢复文件
    恢复到上次提交，不删除本地修改
    git reset file (unstage)
    恢复到上次提交，不删除本地修改
    git reset --soft HEAD^
    删除本地修改
    git reset --hard HEAD
    git checkout HEAD
    git checkout -- <file>

#### 不产生新提交拉取远程代码
    git rebase origin/master(no new commit)

#### 查看文件特定位置的修改记录
    文件3-5行
    git blame -L 3,5 file
    特定行开始的三行
    git blame -L '^/@pass/',+3 file

#### 迁出到某次tag
    git checkout v1.5
    git checkout tags/v1.5

#### 基于某次提交新建分支
    git branch new_branch HASHID

#### 向远端推送特定分支
    git push origin test_branch
    
#### 从远端拉取提交，但不与本地merge
    git fetch origin...
    
#### 将一个分支变基到master
    git rebase master feature
    
#### 优化打包，删除不必要的包
    git repack -d
    

