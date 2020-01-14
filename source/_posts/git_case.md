# git 相关问题

## git 默认不区分大小写问题
* 原因：估计是为了兼容`windows`和`mac os`.
* 参考：https://www.zhihu.com/question/57779034
* git mv 操作来避免 git 未识别：
* `git mv myfolder tmp git mv tmp MyFolder`
* 或者，修改git config
* `git config core.ignorecase false`

## git 清除历史提交
* `git checkout --orphan latest_branch`. 假如你的某个分支上，积累了无数次的提交，你也懒得去打理，打印出的log也让你无力吐槽，那么这个命令将是你的神器，它会基于当前所在分支新建一个赤裸裸的分支，没有任何的提交历史，但是当前分支的内容一一俱全。新建的分支，严格意义上说，还不是一个分支，因为HEAD指向的引用中没有commit值，只有在进行一次提交后，它才算得上真正的分支。
* 1.Checkout
   git checkout --orphan latest_branch
*  Add all the files
   git add -A
*  Commit the changes
   git commit -am "commit message"
*  Delete the branch
   git branch -D master
* Rename the current branch to master
   git branch -m master# 
* Finally, force update your repository
   git push -f origin master
* 这时候，从其他分支合并这个干净分支的时候，如果出现提示：`fatal: refusing to merge unrelated histories`，那么可以用以下命令来合并：`git merge master --allow-unrelated-histories`
* 或者`git push`报`fatal: refusing to merge unrelated histories`,`git pull origin master --allow-unrelated-histories`