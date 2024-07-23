克隆仓库：

```bash
git clone <git地址> 
```

初始化仓库：

```bash
git init 
```



### 提交

添加文件到暂存区：

```bash
git add -A 
```

把暂存区的文件提交到仓库：

```bash
git commit -m "提交信息" 
```

查看提交的历史记录：

```bash
git log --stat 
```



### 项目维护

工作区回滚：

```bash
git checkout <filename> 
```

撤销最后一次提交：

```bash
git reset HEAD^1 
```

> HEAD^n表示COMMIT列表里栈顶的第几个



### 分支

以当前分支为基础新建分支：

```bash
git checkout -b <branchname> 
```

列举所有的分支：

```bash
git branch
```

单纯地切换到某个分支：

```bash
git checkout <branchname> 
```

删掉特定的分支：

```bash
git branch -D <branchname> 
```

合并分支：

```bash
git merge <branchname> 
```

放弃合并：（当出现合并冲突时可使用）

```bash
git merge --abort
```



### Git与Github远程仓库

推送当前分支最新的提交到远程：git push 

拉取远程分支最新的提交到本地：git pull

> 注意：如果推送版本与远端github中的不一致，会默认先从远端pull到本地进行**合并**（注意是合并而不单纯覆盖，与merge操作一致），只有在本地与远端同步且领先于远端时，git才会push到远端github中。

#### 将本地仓库上传到Github仓库

```
# 将本地仓库与远程仓库建立关联（其中origin为远程仓库别名）
git remote add origin https://github.com/bepluvia/CS-Notes.git
# 将当前（本地）分支强制命名为main
git branch -M main
# 将本地main分支推送到远端"origin"仓库，并建立本地分支与远程分支的关联关系
# -u：选项，表示在推送的同时建立本地分支与远程分支的关联关系（upstream）
# 通常在第一次推送本地分支到远程仓库时使用，建立起追踪关系后，之后可以简化推送操作，
# 只需使用git push即可将本地分支的提交推送到远程仓库对应的分支
git push -u origin main
```