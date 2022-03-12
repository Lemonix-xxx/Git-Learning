开摆了！2022.3.12

## 准备

- ssh密钥
```bash
git config --global user.name "name"
git config --global user.email "email"
ssh-keygen -t rsa -C "email"
cd ~/.ssh
# 如果是root目录请转到home下
cat id_rsa.pub
```

- 初始化
> git init


## 远程

- 绑定远程仓库
> git remote add origin 地址

- 查看远程仓库
> git remote -v

- 删除远程仓库
> git remote rm origin

- 推送到当前分支
> git push origin 分支
> 第一次push要 *-v*

- 拉取当前分支
> git pull origin 分支


## 工作区和暂存区

- 查看修改
> git diff

- 查看工作区状态
> git status

- 添加修改文件
> git add 文件名

- 把暂存区都提交到版本库中
> git commit -m "更新内容"


## 版本库

- 查看提交记录
> git log

- 回退 (版本库)
```bash
git reset --hard 版本
# HEAD指当前版本
# HEAD^指上一个版本
# HEAD~100表示上100个版本
```
- 查看回退记录
> git reflog
