# git 工作流

[git工作流相关文档](https://github.com/xirong/my-git/blob/master/git-workflow-tutorial.md)

## 集中式工作流

1. a提交，b需要`git pull --rebase`进行变基操作来避免三方合并
2. 冲突时需要结局冲突。编辑冲突的文件
3. `git add` 然后 `git rebase --contionue`

## 功能分支工作流

1. 克隆master
2. 创建新的分支并切换到该分支`git checkout -b feat-dialog`
3. 在该分支上进行操作并提交`git push -u origin feat-dialog`
4. pull request 进行修改，完成

## Gitflow工作流

## Forking分布式工作流

1. fork项目
2. clone项目到本地,本地提交修改`pull request`
3. 在本地添加对应的远程仓库`git remote add upstream git@github.com:sunshaochen/Test`
4. 当主仓库发生更改时，本地 `git pull upstream master` 然后`git push`  
 

