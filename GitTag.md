# Git Tag


- 在当前提交上，打标签foo,(添加哈希值可以给某个版本添加标签)  
  `git tag foo [hash value]`
- 在当前提交上，打标签foo,并给标签添加信息    
  `git tag foo -m 'msg'`
- 删除标签   
  `git tag -d tagname`
- 查看所有标签  
  `git tag`
- 把标签推送到远程仓库  
  `git push origin --tags`  
  `git push origin --tagname`
- 删除远程仓库的标签  
  `git push origin :refs/tags/v0.1`