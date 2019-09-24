# 如何删除子模块
* 删除.gitmodules文件
* 执行命令：`git rm --cached modulepath`
* 重新将模块添加到`stage`：`git add modulepath/`，记住这里，需要加一个`/`，代表是将文件添加进去，而不是模块。