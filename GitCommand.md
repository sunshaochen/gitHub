# git command
---
- git 命令信息  
- git help -a 查看全部git自命令
- git blame 查看某个文件的修改历史
  - `git blame <file name>` 逐行查看文件的修改历史   
  - `git blame -L 100,110 <file name>` 逐行查看从100-110行文件的修改历史
- git clean 撤销提交
  - `git clean -n` 列出打算删除的档案
  - `git clean -f` 这正删除
  - `git clean -x -f` 连.gitignore中忽略的档案页清除
- `git status -sb` 简短模式显示状态
- git add  
  - `git add  <file name..>` 将文件提交到暂存区
  - `git add .` 将所有的变更都提交到暂存区
  - `git add -p ` 一个文件多个提交
- git commit
  - `git add. + git commit -m  'msg'` == `git commit -a -m 'msg'` == `git commit -am 'msg'`
  - 这里查看: [commit规范](CommitMsg.md)
- git show 
  - `git show HEAD` 查看第一条提交信息
  - `git show HEAD~` 前看前一个提交信息（~3就前3个）
- git log 
  - `git log --oneline -4`
  - `git log <file name>`
  - `git log --grep  <想要筛选的内容>`
  - `git log -n`  要显示的条数
- git diff
  - `git diff` 工作目录和暂存区的区别
  - `git diff --chached` 暂存区和最新版本的区别
  - `git diff HEAD` 工作区和最新版本的区别
  - `git diff <版本号1> <版本号2>` 两个版本之前的区别
  - `git diff HEAD~2 HEAD~3` 两个版本之前的区别
  - `git tag yourTagName HEAD~2`   >> `git diff yourTagName`
  - `git diff --chached yourTagName`
---
## 回撤操作
- 回撤上一次提交  
  `git add.`  
  `git commit --amend -m 'msg'`

- 变基操作，改写历史提交  
  `git rebase -i HEAD~3`
- 回撤暂存区内容到工作目录  
  `git reset HEAD`
- 回撤提交到暂存区    
  `git reset HEAD^1 --soft`
- 回撤提交，放弃变更  
  `git reset HEAD --hard`
- 回撤远程仓库, -f 即 --force  
  `git push -f`
  
---
## 分支操作
- `git branch`  列出当前分支   
	- `git branch iss53` 添加一个名为iss53的分支
	- `git branch -v`  查看当前分支提交的版本
	- `git branch -d hotfix` 删除hotfix分支
	- `git branch -D hotfix` 直接删除hotfix分支
	- `git branch -m old_name new_name 改分支名
	- `git branch -M old_name new_name 强制改分支名
  - `git branch -r` 列出远程分支		
  - `git branch --merged` 列出已经合并的分支
  - `git branch --no-merged` 列出没有合并的分支
  - `git branch -r --merged` 列出远程合并的分支
		 
- `git checkout -t origin/foo`  
    取出远程foo分支

- `git checkout isss53`  
	   切换到ISS53分支
	
- `git push origin <spacs>:<remote branch>`
 	 `git fetch -p`  
     删除远程分支
     
- `git push -u origin branchName`
   添加本地分支到远程
		
- `git merge hotfix` 合并hotfix分支  
  `git merge --no-ff` 合并分支，拒绝fast forward,产生合并commit
- `git checkout -b foo` 创建分支并切换到foo分支

- `git stash` 保存进度
  - `git stash pop` 弹出进度
  - `git stash list` 查看进度列表
  - `git stash clear` 删除stash列表
 
### 冲突
