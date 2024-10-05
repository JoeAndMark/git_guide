# 6 协同工作

[TOC]

## 6.1 Fort 与 Pull Request

### 6.1.1 什么是 Fork

Fork 是 GitHub、Gitee 等平台提供的一种功能，用于创建项目的副本。Fork 后的仓库独立于原始仓库，可以在其中自由地进行开发和实验，而不影响原始仓库。

### 6.1.2 创建 Fork

1. 访问原仓库，在浏览器中打开你想要 Fork 的仓库页面。
2. 点击 Fork 按钮：在仓库页面的右上角点击 `Fork` 按钮，这会在你的 GitHub 账户下创建一个副本。

### 6.1.3 克隆 Fork 的仓库

在本地计算机上克隆你 Fork 的仓库：

```bash
git clone https://github.com/your-username/forked-repo.git
```

### 6.1.4 创建 Pull Request

1. 创建新分支：在本地仓库中创建一个新分支进行开发

```bash
git checkout -b new-feature
```

2. 开发并提交：在新分支上进行开发，并提交你的更改

```bash
git add .
git commit
```

3. 推送到远程仓库：将你的分支推送到 Fork 的仓库

```bash
git push origin new-feature
```

4. 创建 Pull Request：在 GitHub 上打开你 Fork 的仓库，找到你刚刚推送的分支，点击 `Compare & pull request` 按钮，填写必要的信息并提交 Pull Request。

## 6.2 代码审查与合并请求

代码审查（Code Review）是确保代码质量的重要环节。团队成员可以通过 Pull Request 进行代码审查。

### 6.2.1 代码审查流程

1. 查看 Pull Request：打开 Pull Request 页面，查看更改的代码
2. 添加评论：在代码的特定行添加评论，指出潜在问题或提出修改建议
3. 请求修改：如果发现问题，可以请求提交者进行修改。
4. 批准合并：如果代码没有问题，可以批准合并。

### 6.2.2 合并 Pull Request

1. 解决冲突：如果存在冲突，需要解决冲突后再合并
2. 合并：点击 `Merge pull request` 按钮，将更改合并到目标分支
3. 删除分支：合并完成后，可以删除已合并的分支以保持仓库整洁

## 6.3 解决冲突

在多人协作中，冲突是不可避免的。当多个分支修改了相同的文件内容时，就会产生冲突。

### 6.3.1 检查冲突

尝试合并分支时，如果存在冲突，Git 会提示冲突信息。

```bash
git merge feature-branch
```

### 6.3.2 解决冲突

1. 打开冲突文件：用文本编辑器打开冲突文件，找到冲突标记。

```bash
<<<<<<< HEAD
// 当前分支的更改
=======
// 要合并的分支的更改
>>>>>>> feature-branch
```

2. 手动解决冲突：根据需要修改冲突内容，删除冲突标记

3. 标记解决冲突：修改完成后，添加并提交解决冲突的文件

```bash
git add confilcted-file
git commit
```

## 6.4 使用 Issue 跟踪任务

在 GitHub、Gitee 等平台上，可以使用 Issue 来跟踪任务和 Bug。

### 6.4.1 创建 Issue

1. 打开 Issue 页面：在仓库页面上，点击 Issues 标签。
2. 新家 Issue：点击 `New issue` 按钮，填写标题和描述，提交 Issue。

### 6.4.2 处理 Issue

1. 分配任务：将 Issue 分配给团队成员
2. 谈论：在 Issue 页面上进行讨论，提出解决方案。
3. 关闭 Issue：完成任务或修复 Bug 后，关闭 Issue。