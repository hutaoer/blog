# git 默认不区分大小写问题
* 原因：估计是为了兼容`windows`和`mac os`.
* 参考：https://www.zhihu.com/question/57779034
* git mv 操作来避免 git 未识别：
* `git mv myfolder tmp git mv tmp MyFolder`
* 或者，修改git config
* `git config core.ignorecase false`