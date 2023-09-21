# 初始化

1. 创建本地git仓库

```

git init

```

操作成功后会生成一个隐藏文件.git, 在文件夹中打开"显示隐藏文件"即可查看

2. 登录GitHub账号(第一次使用Git)

```

git config --global user.name 用户名

git config --global user.email 邮箱地址

```

3. 更改本地分支名称

```

git branch -m master main

```

因为一些政治因素, github原本的主分支从master改成了main, git还没改

4. 关联远程仓库

```

git remote add origin 远程仓库地址

```

origin为自定义的仓库名称

5. 建立本地仓库分支与远程仓库分支联系

```

git push --set-upstream origin main

```

  

# 其他常用指令

### 提交操作

- 将文件添加到暂存区

```

git add .

```

.  代表当前目录所有文件, 注意 'add .' 中间有个空格

  

- 提交到本地仓库  

```

git commit -m 备注信息  

```

m 代表 meassage, 可以理解为每次提交的备注内容

  

- 推送到远程仓库的主分支

```

git push origin main

```

origin为仓库名 master为分支名

- 拉取远程仓库更新本地仓库
```
git pull origin main
```

- 克隆项目到本地仓库  

```

git clone 项目地址  

```

### 分支操作

* 查看分支
```
git branch                           --查看本地分支
git branch -a/git branch --all       --查看本地及远程仓库分支
```
*注意:
git init后, 需要先执行一次git add .和git commit,再使用git branch, 才会显示本地分支

**因为git的分支必须指向一个commit, 没有任何commit就没有任何分支, 提交第一个commit后git自动创建master分支

- 新建分支  

```

git branch 分支名  

```

- 切换分支

```

git checkout 分支名

```

- 新建的同时切换到该分支  

```

git checkout -b 分支名

```

- 合并分支

指定一个分支合并到当前选定的分支，产生冲突时需选择保留哪一个分支  

```

git merge 指定分支名称

```

例如当前在master分支，git merge dev即把dev分支合并到master分支中    

- 删除分支  

```

git branch -d 分支名

```