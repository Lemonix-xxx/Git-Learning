开摆了！2022.3.11

## 准备

- ssh密钥
```
git config --global user.name "name"
git config --global user.email "email"
ssh-keygen -t rsa -C "email"
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

## 工作区和暂存区

- 查看修改
> git diff

- 查看工作区状态
> git status

- 查看提交记录
> git log

- 拉取当前分支
> git pull origin 分支

- 推送到当前分支
> git push origin 分支
> 第一次push要 *-v*

- 回退 (暂存区)
```bash
git reset --hard 版本
# HEAD指当前版本
# HEAD^指上一个版本
# HEAD~100表示上100个版本
```
