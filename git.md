# git



## 一. 简介



主要命令



``` git
add:添加，将代码提交到暂存区
clone:克隆，从远程仓库中克隆代码到本地仓库
checkout:检出，从本地仓库剪出一个仓库分支然后进行修订
commit:提交到本地仓库
fetch:从远程库抓取到本地仓库
pull:从远程库拉到本地库，自动进行合并，然后放到工作区
push:将代码推送到远程仓库
```



打开git bash



基本配置



``` git
// 设置用户邮箱
git config --global user.email "xxxxxx@xx.com"
// 设置用户名
git config --global user.name "xxx"
```



在用户目录下创建.bashrc



然后填写自己需要设置别名的文件



``` bash
alias git-log='git long --pretty =oneline --all --graph --abbrev-commit'
alias ll='ls-al'
```



## 二. 流程



在需要使用git管理的数据中打开git bash窗口



执行命令git init



使用add命令添加到暂存区



然后使用commit来添加到仓库中



中途可以使用git status来查看仓库的状态



通过git log来查看提交记录



通过git reset --hard commitID(通过git log来查看id)



git reflog可以查看已经删除的提交记录



## 三. 分支



git branch 来新建分支



