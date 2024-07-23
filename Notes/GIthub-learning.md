# Github学习

### 将本地仓库上传到Github仓库

```bash
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



### 常用命令

![image-20240602153628014](C:\Users\Pluvia\AppData\Roaming\Typora\typora-user-images\image-20240602153628014.png)

```bash
# 克隆仓库
git clone <git地址>
# 初始化仓库
git init 

# 添加文件到暂存区
git add -A
git add .
# 把暂存区的文件提交到仓库
git commit -m "提交信息"
# 查看提交的历史记录
git log --stat

# 工作区回滚
git checkout <filename>
# 撤销最后一次提交
git reset HEAD^1

# 以当前分支为基础新建分支
git checkout -b <branchname>
# 列举所有的分支
git branch
# 单纯地切换到某个分支
git checkout <branchname>
# 删掉特定的分支
git branch -D <branchname>
# 合并分支
git merge <branchname>

# 推送当前分支最新的提交到远程
git push
# 拉取远程分支最新的提交到本地
git pull
```

