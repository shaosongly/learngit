# 常用 Git 命令速查

本文档按使用场景整理了最常用的 Git 命令，帮助你在日常开发中快速查找所需操作。

## 基础操作

| 命令 | 说明 |
| ---- | ---- |
| `git init` | 在当前目录初始化一个新的 Git 仓库。 |
| `git clone <repo>` | 克隆远程仓库到本地。 |
| `git status` | 查看工作区与暂存区的当前状态。 |
| `git add <file>` | 将文件的修改添加到暂存区。 |
| `git commit -m "message"` | 将暂存区的更改提交到仓库历史。 |
| `git log --oneline` | 用精简格式查看提交历史。 |
| `git show <commit>` | 查看指定提交的详细信息。 |
| `git diff` | 查看工作区、暂存区或两次提交之间的差异。 |

## 分支管理

| 命令 | 说明 |
| ---- | ---- |
| `git branch` | 列出本地分支，或配合参数创建、删除分支。 |
| `git branch -a` | 同时列出本地和远程跟踪分支。 |
| `git checkout <branch>` | 切换到指定分支或检出提交。 |
| `git checkout -b <branch>` | 基于当前分支新建并切换到一个分支。 |
| `git switch <branch>` | 切换到指定分支（Git 2.23+ 推荐写法）。 |
| `git switch -c <branch>` | 创建并切换到新分支。 |
| `git merge <branch>` | 将指定分支合并到当前分支。 |
| `git rebase <branch>` | 以另一分支为基线整理当前分支提交历史。 |

## 远程协作

| 命令 | 说明 |
| ---- | ---- |
| `git remote -v` | 查看已配置的远程仓库及其地址。 |
| `git fetch` | 从远程获取最新提交，但不合并到当前分支。 |
| `git pull` | 获取远程更新并合并到当前分支。 |
| `git push` | 将本地提交推送到远程仓库。 |
| `git push -u origin <branch>` | 首次推送并建立与远程分支的跟踪关系。 |
| `git push --force-with-lease` | 在确保安全的情况下强制推送。 |

## 常用排错与清理命令

| 命令 | 说明 |
| ---- | ---- |
| `git stash` | 暂存当前未提交的更改，保持工作区干净。 |
| `git stash pop` | 恢复最近一次 `stash` 并从列表中移除。 |
| `git reset HEAD <file>` | 将暂存区中的文件移出，保留工作区改动。 |
| `git checkout -- <file>` | 放弃工作区中对某个文件的改动。 |
| `git revert <commit>` | 生成一个新的提交，用于撤销指定提交。 |
| `git clean -fd` | 删除未跟踪的文件与目录（危险操作，请谨慎使用）。 |

> 提示：使用 `git help <command>` 或 `git <command> --help` 可以查看任意 Git 命令的详细说明和示例。
