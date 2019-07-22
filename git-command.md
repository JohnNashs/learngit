# Git 常用指令
*傅宇敏* 2019-07-22

## 创建版本库

```bash
git init
```

## 添加远程库
```bash
$ git remote add origin https://github.com/JohnNashs/learngit.git
```

## 克隆指定分支
```bash
git clone -b <name> 仓库地址
```

## Git 状态

```bash
git stauts
```

## 三种状态

- Working Directory 工作区
- Staging Area 暂存区
- Repository 版本库

## 精简命令

### 提交代码

```bash
# 将代码提交到暂存区
git add .

# 将代码提交到当前分支
git commit -m "这里是注释"

# 将代码提交到线上
git push
```

### 拉取代码

```bash
git pull
```

### 分支操作

```bash
# 查看分支
git branch

# 新建分支
git branch NewBranchName

# 切换分支
git chekcout NewBranchName

# 本地检出一个新的分支并推送到远程仓库

## 1.创建并切换分支（创建本地分支）
git checkout -b <name>
## 2.创建并切换分支（创建本地分支）
git push --set-upstream origin <name>

# 将远程git仓库里的指定分支拉取到本地（本地不存在的分支）
git checkout -b 本地分支名 origin/远程分支名

# 合并某支到当前分支
git checkout master #先切换到master
git merge NewBranchName #将NewBranchName合并到当前的分支master

# 删除分支
git branch -d NewBranchName
```

### 查看log

```bash
# 查看 commit log
git log

# 查看操作记录
git relog # git log -g
```

### 版本回退

```bash
# 回退若干个版本(回退一个 HEAD^, 回退两个版本是 HEAD^^, 三个是 HEAD^^^, 以此类推 )
git reset --hard HEAD^

# 按照版本号回退
git reset --hard HEAD~版本号 # 版本号不需要写全
```

## 原则

协同开发应建立自己的分支，再合并到master上

## 教程

[Git官网](https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-Git-%E5%9F%BA%E7%A1%80)

[廖雪峰](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

