# 如何在git上创建本地分支

1. 从已有的分支创建新的分支(如从master分支),创建一个ipps1229分支

```
Git checkout -b ipps1229


备注：也可以换成以下两步
git branch ipps1229
git checkout ipps1229 
```

2. 将ipps1229分支推送到远程

```
git push origin ipps1229:ipps1229

​ 冒号前面的ipps1229: 推送本地的ipps1229分支到远程origin
​ 冒号后面的ipps1229: 远程origin没有则会自动创建
```

3. 建立本地到远程仓库的连接，然后推送代码
```
$ git push --set-upstream origin ipps1229
```

4. 取消对 master 分支追踪
```
$ git branch --unset-upstream master
```

# 附录
- 删除本地分支
```
$ git branch -d dev
```
- 删除远程分支
```
$ git push origin --delete dev
```

- git branch命令

```
git branch branchName(在本地创建一个命名为branchName的分支)
git branch 查看当前自己所在的分支
git branch -a 查看服务器的所有分支以及自己当前所在的分支
```

- 推送命令
```
git push origin branchName(把命名为branchName的本地分支推送到服务器)
```

- 切换

```
git checkout --track origin/branchName (切换为远程服务器上的命名为branchName的远程分支)

 如果你的搭档要把他本地的分支给关联到服务器上命名为branchName的远程分支，请执行以下操作，
git branch --set-upstream localBranchName origin/branchName  
（为本地分支添加一个对应的远程分支 与之相对应）->这行命令用来关联本地的分支与服务器上的分支
```



- Git 全局设置
```
git config --global user.name "well"
git config --global user.email "welllife3@163.com"
```
