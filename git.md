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



git branch :来查看分支



git branch 分支名 :来新建分支



git checkout 分支名:  切换分支



git checkout -b 分支名 创建并切换分支 



git merge 分支名称



git branch -d b1 删除分支时需要检查



git branch -D b1 不需要检查



## 四. 开发中的原则和流程



1. master分支
2. develop分支
3. featrue
4. hotfix
5. test
6. pre



## 五. git远程仓库



配置公钥



ssh-keygen -t rsa 生成



然后输入y一路回车就可以了



cat ~/.ssh/id_rsa.pub 复制到GitHub或者码云当中的ssh中



git remote add origin 加仓库地址



git remote 在使用这个语句



git push origin 分支名



如果远程分支名和本地分支名相同则可以致谢本地分支



-f参数表示强势覆盖



--set -upstream 推送到远程的同时建立起和分支之间的关系



如果当前分支和远程分支关联，则可以省略分支名和远程名



## 六. 远程操作



git clone <仓库路径> [本地目录]



本地目录可以省略



git fetch [remote name] [branch name]



将仓库中的更新都抓到本地，不会进行合并，如果不指定远端名称和分支名则抓取所有分支



git pull



自动进行合并
