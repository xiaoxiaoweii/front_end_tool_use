## 分支操作

- 显示本地所有分支以及当前所在哪个分支

  ``` shell
  git branch
  ```

- 新建名为 branchName 的新分支

  ``` shell
  git branch branchName
  ```

- 删除名为 branchName 的分支

  ```shell
  git branch -d branchName
  ```

- 强制删除分支branchName

  ``` shell
  git branch -D branchName
  ```

## 分支切换

- 从当前分支切换到名为 branchName 的分支上

  ```shell
  git checkout branchName
  ```

- 新建名为 branchName 的分支并切换到该分支上。

  ``` shell
  git checkout -b branchName
  ```


## 合并分支

- 将名为 branchName 的分支合并到当前分支。

  ```shell
  git merge branchName
  ```

## 分支的变基

- 当前分支 rebase 到 master 分支

  ``` shell
  git rebase master
  ```

- 将 dev 分支 rebase 到 master 分支

  ```shell
  git rebase master dev
  ```

- 与 merge 操作的区别
  - rebase 操作 节点拿下来换了一个位置重新放。最后不会产生合并的痕迹，所有分支都是同一条直线。

## 挑拣节点合并到当前分支上

- 从其他分支上挑拣某些节点到当前分支

  ``` shell
  git cherry-pick commit_id
  ```
