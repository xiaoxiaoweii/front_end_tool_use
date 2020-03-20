## 1. 环境设置命令

```shell
$ git config --global user.name "" // 设置用户名称
$ git config --global user.email "" // 设置邮件地址
```

- 使用`--global`参数表示设置了全局的环境，特定的项目使用不同的用户名和邮件地址，在该项目目录下不使用`--global`参数设置不同的用户名和邮件地址。

```shell
$ git config --list // 列出当前Git所有的配置信息
// 显示配置信息
core.symlinks=false                                               core.autocrlf=true                                                 core.fscache=true                                                 color.diff=auto                                                   color.status=auto                                                 color.branch=auto                                                 color.interactive=true                                             help.format=html                                                   rebase.autosquash=true                                             http.sslcainfo=C:/Program Files/Git/mingw64/ssl/certs/ca-bundle.crt              
http.sslbackend=openssl                                           diff.astextplain.textconv=astextplain                             filter.lfs.clean=git-lfs clean -- %f                               filter.lfs.smudge=git-lfs smudge -- %f                             filter.lfs.process=git-lfs filter-process                         filter.lfs.required=true                                           credential.helper=manager                                         user.email=2679656468@qq.com                                       user.name=xiaoxiaoweii                                              core.autocrlf=false                                               core.repositoryformatversion=0                                     core.filemode=false                                               core.bare=false       
```

## 2. 初始化本地仓库

- 进入项目的目录下执行命令，就可以初始化成一个 Git 仓库了。

  ```shell
  $ git init
  ```

## 3. 克隆远程仓库到本地

- 该项目从远程克隆到本地

  ```shell
  $ git clone git@github.com:xiaoxiaoweii/front_end_tool_use.git // 通过ssh方式克隆 只要拿到该项目的 url 可以随便 clone，但是在 push 到远程的时候需要验证用户名和密码；
  $ git clone https ://github.com/xiaoxiaoweii/front_end_tool_use.git // 通过https方式克隆 需要现电脑的SSH key（SSH公钥）添加到GitHub上，在 clone 项目和 push 项目到远程时都不需要输入用户名和密码。
  ```

## 4. 生成SSH公钥

- 检查电脑中是否有公钥，一般在`~/.ssh/`目录下。目录下存在`id_rsa.pub`文件，这就是公钥（id_rsa 文件是私钥）；如果不存在此文件或者`.ssh`目录也不存在，需要用 ssh-keygen 命令来生成。

- 生成SSH key命令

  ```shell
  $ ssh-keygen
  ```

  - 公钥`id_rsa.pub`文件的内容

    ```shell
    ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCYx46muC8s9rC3QY2HdIOVpdVwxajXdoylw8yhy+rDFEwxoRCbfJFxGftGUFxjmVArfaIB3se/JKQwZve+peVSqEkIwtKfi6gfheV9igIpy16gINIspydB6nMlKudFmRKXn/2wH8YvZ5jqNLhRcVkf/kaOPFmVzPgyQnMVtymtq5dXLMMP2DC94QvDSW8RBmi10zFSx2++0GTdenv4+SGr22PK7zzehjT6J/xu1c9r7AGUPnQUldAQDBTLAMsCJ+GjZOz/HhiRUBLrLbhSkXwHzfdKRddnMdGIykttg/mIavCj+DO+/5uHzKy0YdpFJZWJfiNHE6QaVPaqN1aRcK8b 2679656468@qq.com
    ```

- 在Github中将公钥添加即可 [GitHub添加公钥](<https://www.jianshu.com/p/106305921b90>)

## 5. 查看当前状态

```shell
$ git status // 显示当前所处的分支，以及当前工作区是否干净，是否有文件要提交。
```

## 6. 添加到暂存区

```shell
$ git add xxxxx    //后面接文件名，表示将某个文件添加到暂存区   
$ git add .                 //后面接一个点，表示将全部文件添加到暂存区
```