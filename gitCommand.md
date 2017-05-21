# git command
---
* git 命令信息  
* git help -a 查看全部git自命令 
* git blame
  * git blame `<file name`> 逐行查看文件的修改历史   
  * git blame -L 100,110 `<file name`> 逐行查看从100-110行文件的修改历史
* git clean
  * git clean -n 列出打算删除的档案
  * git clean -f 这正删除
  * git clean -x -f 连.gitignore中忽略的档案页清除
* git status -sb 简短模式显示状态
* git add 
  * git add  `<file name..`> 将文件提交到暂存区
  * git add . 将所有的变更都提交到暂存区
  * git add -p 一个文件多个提交
* git commit
  * git add. + git commit -m  'msg' == git commit -a -m 'msg' == git commit -am 'msg'
  * [commit规范](commitMsg.md)
