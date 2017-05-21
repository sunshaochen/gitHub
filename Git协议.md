# Git协议

---
## 本地协议

* 克隆本地仓库   
 git clone /c/wd/test.git
* 克隆本地仓库，不建议使用file://   
 git clone file:///c/wd/test.git
* 添加远程仓库的链接   
  git remote add origin /c/wd/test.git


## git协议

* 克隆远成仓库  
 git clone git://server_ip/test.git
* 添加远程仓库的链接  
 git remote add origin git://server_ip/test.git
 
## http协议

* 克隆远程仓库  
 git clone https://github.com/sunshaochen/test.git
* 添加远程仓库的链接  
 git remote add origin https://github.com/sunshaochen/test.git


## ssh协议

* 克隆远程仓库，一般写成简短的命令  
 git clone ssh://git@github.com/sunshaochen/test.git  
 git clone git@github.com:sunshaochen/test.git
 
* 添加远程仓库的链接  
 git remote add origin git@github.com:sunshaochen/test.git
