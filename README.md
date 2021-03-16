## Git command manual

#### 查看 git 版本号

```shell
git --version
```

#### Git 配置信息

```shell
# 查看仓库配置（要在仓库目录下）
git config --local -l
# 查看用户信息
git config --global -l
# 查看系统信息
git config --system -l 
# 查看所有配置信息
git config -l
```

#### 添加配置信息

```shell
# 添加邮箱
git config --global user.email “you@example.com”
# 添加用户名
git config --global user.name “Your Name”
```

#### 创建新的 Git 仓库

```shell
mkdir test
cd test/
git init
Initialized empty Git repository in /e/hamming/test/.git/
# 初始化空 Git 仓库完毕。
```

#### 分支管理

```shell
# 创建分支
git branch newBranch
# 切换分支
git checkout branchName
# 更新远程仓库信息
git fetch origin
# 拉取远程分支并创建新的分支
git checkout -b newBranch remote/branch
# 创建并切换到当前分支
git checkout -b newBranch
# 分支重命名(M:即使分支名称已存在)
git branch -m/M oldName newName
# 删除分支(git branch --delete --force)
git branch -D branchName
# 删除分支(删除前检查merge状态)
git branch -d branchName 
# 将branchName merge到当前分支
git merge branchName
```

#### 远程分支

```shell
# 推送内容到远程分支
git push (remote) (branch)
# 拉取远程分支内容到当前分支
git pull remote branch
# 删除远程分支
git push origin --delete branchName
```

#### 远程仓库操作

```shell
# 添加远程仓库
git remote add [aliaName] [url]
# 查看远程仓库信息
git remote -v
# 删除远程仓库
git remote rm name
# 修改仓库名
git remote rename old_name new_name  
```
