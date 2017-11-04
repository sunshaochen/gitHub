# GitConfig


## username&email
`git config --global user.namec"孙韶辰"`  
`git config --global user.emailc"sunscsmail@gmail.com"`


## ignore config 
将某些文件忽略版本控制，添加 **.gitignore** 文件  
内容如下：  
  `.progect`  
  `*.md.html` 
  
##　windows系统下忽略crlf告警
`git config --global core.safecrlf false`  

## 设置别名
`git config --global alias.ci commit`
`git config --global alias.hi log --pretty=format:'%h %ad | %s%d [%an]' --graph`

---

`cd ~`  
`vim .gitconfig`  

`ci = commit`  
`ad = add .`  
`br = branch`  
`hi = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short`  
`st = status` 



