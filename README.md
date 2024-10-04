# Git 入门教程
[TOC]

## 1 简介

本教程的主要目的系让大家快速入门 Git，掌握其基本使用方法和常规操作，而非深入讨论 Git 的内部实现细节。

通过本教程，您将能够轻松应用 Git 进行版本控制，提高团队协作效率。

如果您想要了解更多关于 Git 的信息，可以通过以下方式：

+ GitHub 官方托管仓库：[git/git](https://github.com/git/git)
+ Git 官网：[https://git-scm.com/](https://git-scm.com/)
+ Pro Git 书籍（免费在线版）：[Pro Git](https://git-scm.com/book/en/v2)
+ Git 教程和文档：[Git Documentation](https://git-scm.com/doc)
+ Git 社区及支持：[Git Community](https://git-scm.com/community)

## 2 合集目录

1. [简介]()
2. [安装与配置]()
3. [Git 基础操作]()
4. [分支与合并]()
5. [远程仓库]()
6. [协同工作]()
7. [标签与版本发布]()
8. [高级操作]()
9. [Git 工具与扩展]()
10. [常见问题与故障排除]()
11. [资料与学习资料]()

## 3 其他

本教程的开源文档和更多内容可以在我的 GitHub 仓库中找到。如果您觉得本教程对您有帮助，不妨点个 Star 支持一下！

- 我的 GitHub 开源地址：[JoeAndMark/git_guide](https://github.com/JoeAndMark/git_guide)

如果您在学习过程中发现任何错误或有任何改进建议，欢迎随时提出。您可以在 [Issues](https://github.com/JoeAndMark/git_guide/issues) 中提交您的反馈，我会尽快处理。

感谢您的支持和鼓励！期待大家共同进步！

如果您想要贡献自己的想法，请遵循以下提交约定。

### 3.1 提交约定

#### 3.1.1 提交信息格式

提交信息的结构如下所示：

```text
<类型>[可选 范围]: <描述>

[可选 正文]

[可选 脚注]
```

#### 3.1.2 类型

提交信息的类型只应从如下类型中选择：

+ `feat`：新增章节或主要内容
+ `fix`：修正错误或拼写
+ `docs`：更新使用说明或参考文献
+ `style`：格式化或排版调整
+ `refactor`：重组章节或内容调整
+ `test`：添加或修改书籍的测试材料（如练习题）
+ `chore`：其他维护性任务，如更新工具或配置

提交示例：

+ `feat: 添加第一章内容`
+ `fix: 修正错误或拼写`
+ `docs: 更新参考文献列表`
+ `style: 调整章节标题格式`
+ `refactor: 重新组织第三章结构`
+ `test: 添加第四章的练习题`
+ `chore: 更新 LaTeX 模版`

> [!note]
>
> 注意：`<类型>` 后的冒号（`:`）应为英文输入法下的冒号，而非（`：`）

#### 3.1.3 Conventional Commits

本仓库的提交约定基于 Conventional Commits 进行修改，如果您想要了解更多关于 Conventional Commits 的信息，可以通过以下方式：

+ GitHub 官方托管仓库：[conventional-commits/conventionalcommits.org](https://github.com/conventional-commits/conventionalcommits.org)
+ 官方网站：[Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

