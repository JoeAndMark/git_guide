# 5 远程仓库

[TOC]

远程仓库是存储在网络上的 Git 仓库，通常用于团队协作和备份。常见的远程仓库托管服务由 GitHub、GitLab 和 Gitee 等。

## 5.1 添加远程仓库

在开始与远程仓库交互之前，需要先添加一个远程仓库。假设我们有一个远程仓库的 URL，如 `https://github.com/username/repo.git`

1. 查看当前的远程仓库

```bash
git remote -v
```

这条命令会列出当前配置的所有远程仓库及其  URL。

2. 添加远程仓库

```bash
git remote add origin https://github.com/username/repo.git
```

在这里，`origin` 是远程仓库的名称（别名），您可以用其他名字替换它，但 `origin` 是惯例。

## 5.2 推送与拉取

一旦配置了远程仓库，接下来就可以将本地的更改推送到远程仓库，或从远程仓库拉取最新的更改。

1. 推送更改

```bash
git push origin master
```

这条命令将本地 `master` 分支的更改推送到远程仓库的 `master` 分支。首次推送时，可能需要使用 `-u` 选项将本地分支与远程分支关联起来。

```bash
git push -u origin master
```

2. 拉取更改

```bash
git pull origin master
```

## 5.3 同步

为了确保本地仓库与远程仓库保持同步，可以使用一下命令：

1. 获取最新的远程仓库信息

```bash
git fetch origin
```

> [!Note]
>
> 注意：`git fetch` 只会下载远程仓库的最新状态到本地，但不会自动合并这些更改。

2. 拉取并合并更改

```bash
git pull origin master
```

`git pull` 实际上是 `git fecth` 和 `git merge` 的组合。它会获取远程仓库的最新更改，并自动尝试将其合并到当前分支。

3. 变基操作

有时，您可能希望将本地的更改应用到最新的远程仓库基础上，而不是自动合并，这时候可以使用 `rebase`：

```bash
git pull --rebase origin master
```

`--rebase` 选项会将本地的更改重新应用到远程分支的最新状态上，从而保持更直线的提交历史。

## 5.4 远程仓库管理

1. 查看远程仓库详细信息

```bash
git remote show origin
```

这条命令会显示关于 `origin` 远程仓库的详细信息，包括其 `URL`、跟踪的分支等。

2. 重命名远程仓库

```bash
git remote rename origin new-origin
```

这条命令会将远程仓库 `origin` 重命名为 `new-origin`。

3. 移除远程仓库

```bash
git remote remove origin
```

这条命令会移除名为 `origin` 的远程仓库。