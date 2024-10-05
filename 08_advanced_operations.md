# 8 高级操作

[TOC]

## 8.1 变基

变基（Rebase）是一种将一个分支上的提交应用到另一个分支的技术。它可以用来清理提交历史，使历史更加线性和易读。

假设你有一个名为 `feature` 的分支，它是从 `main` 分支分出来的。`main` 分支有一些新的提交，你希望将这些提交包含到 `feature` 分支中。

1. 切换到 `feature` 分支：

```bash
git checkout feature
```

2. 运行变基命令：

```bash
git rebase main
```

这会将 `feature` 分支上的所有提交重新应用在 `main` 分支的最新提交之后。此过程可能会出现冲突，需要手动解决冲突后继续变基。

解决冲突后继续变基：

```bash
git add <冲突文件>
git rebase --continue
```

放弃变基：

```bash
git rebase --abort
```

## 8.2 暂存更改

暂存更改（stash）允许你保存当前工作目录的未提交更改，以便在以后应用。它对于在处理一个任务时突然需要切换到另一个任务非常有用。

1. 暂存当前更改：

```bash
git stash
```

2. 查看暂存列表：

```bash
git stash list
```

3. 应用最近一次暂存的更改：

```bash
git stash apply
```

4. 应用并删除最近一次暂存的更改：

```bash
git stash pop
```

5. 删除所有暂存

```bash
git stash clear
```

## 8.3 查看与还原历史版本

Git 提供了几种方法来查看和还原历史版本。

### 8.3.1 查看历史版本

1. 查看提交历史：

```bash
git log
```

2. 查看单行提交历史

```bash
git log --oneline
```

3. 查看某个文件的提交历史

```bash
git log -- <文件名>
```

### 8.3.2 还原历史版本

`git reset` 和 `git revert` 是两种不同的还原提交的方法。

#### Git Reset

`git reset` 用于回撤提交，可以改变提交历史。使用时要谨慎，尤其是在共享的分支上。

1. 软重置（保留工作目录的更改）：

```bash
git reset --soft <提交哈希>
```

2. 混合重置（重置索引区，保留工作目录的更改）：

```bash
git reset --mixed <提交哈希>
```

3. 硬重置（彻底删除更改）：

```bash
git reset --hard <提交哈希>
```

#### Git Revert

`git revert` 创建一个新的提交来撤销指定的提交，这样不会更改提交历史，适合在共享分支上使用。

1. 撤销某次提交：

```bash
git revert <提交哈希>
```

2. 撤销最近一次提交：

```bash
git revert HEAD
```