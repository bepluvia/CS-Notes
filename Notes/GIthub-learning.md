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