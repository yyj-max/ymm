
### 新建代码仓库（云端 github，gitee，etc）
* 创建一个仓库
* 仓库的url：https://github.com/yyj-max/mi.git
### 本地代码上传到新建的云端仓库
* 本地的代码仓库
* 启动Git Bash 命令
* Linux操作命令：

pwd # 显示当前所在的路径

cd 路径  # change directory,进入指定的路径下

* 进入了本地的代码仓库（文件夹）

ls -a # ls:list,-a:all.显示出当前路径下所有的文件及文件夹

* 初始化当前文件夹为一个Git代码仓库

git init

* 添加到本地仓库

git add 文件名
git add.

* 提交到本地仓库，成功会出现仓库记录的变动信息

git commit -m "message"

* 计算机初次使用Git ,会提示配置用户名及登陆邮箱



### 目前完成了本地仓库的代码提交
###  下一步进行远程代码仓库提交

* 提交到哪？远程仓库的地址要添加到本地仓库的配置中。

git remote add origin https://github.com/yyj-max/mi.git/demon-2 # origin 是代码仓库命名 
可以为其他名称。https://github.com/yyj-max/mi.git 是远程代码仓库的地址，

* 完成了远程代码仓库的提交
git push -u origin master # -u origin 指定仓库；master 为远程仓库的代码分之

### 完成了初次从本地到远程的代码提交

### 本地修改了文件（代码、文档），代码仓库的更新

* 修改仓库后
git add 修改的文件名
git commit -m"msg"提交修改的文件
完成了本地的代码仓库更新`
