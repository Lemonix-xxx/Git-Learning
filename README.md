# Lemonix的Git教程
# 这里是Dev分支的README！
既是给大家学习的教程，也是我的学习历程

_2022.3.13更新_

Git仓库网站: [Github](github.com)  [Gitee](gitee.com)

***

## 准备

- SSH密钥
```bash
# 各个系统保存的位置不一样，我这里以Linux为主来演示
git config --global user.name "name"
git config --global user.email "email"
ssh-keygen -t rsa -C "email"
cd ~/.ssh
# 如果是root目录请转到home下
cat id_rsa.pub
# 将内容添加到你的Github或者Gitee上的SSH密钥
```

- 初始化
```bash
git init
# 手动mkdir并进入

git init 目录
# 自动给你mkdir
```


## 远程

- 克隆远程仓库 (别人或者自己的都可以)
> `git clone 地址`

- 绑定远程仓库
> `git remote add origin 地址`
>
> 地址格式: git@网站:仓库地址.git

- 查看远程仓库
> `git remote -v`

- 删除远程仓库
> `git remote rm origin`

- 推送到当前分支
> `git push origin 分支`
>
> **注:** 第一次push要在push后加 *-u*，这样就把本地master分支和远程master分支关联了起来，方便以后操作

- 拉取并与本地分支合并
> `git pull origin 分支`

- 获取远程分支 (不合并)
> `git fetch origin 分支`


## 工作区和暂存区

- 查看修改
> `git diff`

- 查看工作区状态
> `git status`

- 暂存修改文件
> `git add 文件名`

- 撤销修改
```bash
git checkout -- 文件名
#      两边各一个空格
# 如果该文件还没有添加到暂存区，则恢复到版本库
# 如果该文件添加到了暂存区，则撤销提交，但保留修改

git reset HEAD 文件名
# 将文件恢复到版本库
```

- 把暂存区都提交到版本库中
> `git commit -m "更新内容"`

- 删除文件
> `git rm 文件名`


## 版本库

- 查看提交记录
> `git log`

- 回退 (版本库)
```bash
git reset --hard 版本
# HEAD指当前版本
# HEAD^指上一个版本
# HEAD~100表示上100个版本
```
- 查看回退记录
> `git reflog`

## 常见问题

- 第一次`git push`和`git clone`时出现警告怎么办？
> *The authenticity of host 'github.com (xx.xx.xx.xx)' can't be established.
RSA key fingerprint is xx.xx.xx.xx.xx.
Are you sure you want to continue connecting (yes/no)?*
>
> 这是让你确定是否信任该Key，以防有人冒充Github或者Gitee服务器。

- `git rm`和`rm`的区别
> `git rm`会从版本库中删除文件，`rm`只从本地删除，想从版本库删除还要先add。
> `git rm`想要恢复需要`git reset HEAD`，直接`rm`的话需要`git checkout -- 文件名`来恢复。

## 翻译参考
- Branch -> 分支
- Pull -> 拉取
- Fetch -> 获取
- Remote -> 远程
- Merge -> 合并
- Repository -> 仓库
- Push -> 推送
- Commit -> 提交
- Stage -> 暂存区
- Add -> 添加；暂存
- Status -> 状态
- Diff (Differences) -> 修改
- Working tree -> 工作区
- Reset -> 回退；恢复
- Clone -> 克隆；复制

