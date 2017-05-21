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

### SSH配置
1. 生成RSA密钥对  
 ssh-Keygen -t rsa -C "your email"
2. 在Github网站添加公钥
3. 使用ssh协议，克隆仓库或者添加远程链接

如果存在链接超时的情况，解决方法： 
1. 找到git的安装目录，找到/etc/ssh/ssh_config文件
2. 把如下内容复制到ssh_config文件的末尾处并保存  
  Host github.com  
  User git  
  Hostname ssh.github.com  
  PreferredAuthentications publickey  
  IdentityFile ~/.ssh/id_rsa  
  Port 443  
 
