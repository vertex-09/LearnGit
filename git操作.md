# git 操作



## 撤销修改

```shell
简而言之：
原来的工作区 <--------------- 修改后的工作区 <--------------------- 暂存区
             git restore .                git restore staged .
```


### 当更新版本库之后，撤销工作区的修改（还没有add）：

1. 手动 `Ctrl + Z` （没学 `git` 之前的笨办法）
2. `git checkout -- <file>` 或 `git restore <file>`（全选用 `.`）

### 当更新版本库之后，撤销工作区的修改（已经add）：

1. `git reset HEAD <file>`  或 `git restore --staged <file>`（清除掉暂存区）
2. 进行（还没有add）的操作



## 删除文件

1. `git rm <file>`，同时删除工作区和暂存区中的文件，再执行 `git commit` 时，正式记录下文件的删除。



## 分支

1. 查看分支：`git branch`
2. 创建分支：`git branch <name>`
3. 创建+切换分支：`git switch -c <name>` 或者 ~~`git checkout -b <name>`~~
4. 合并某分支到当前分支：`git merge <name>`
5. 删除分支：`git branch -d <name>`
