commit 1
commit 3
## git revert {commit-id} 和 git reset {commit-id}的区别
+ revert是创建一个新的commit，`此次commit`是删除`目标commit`修改的内容，过程中可能出现冲突，需要解决
+ reset是直接将HEAD指向`目标commit`，`目标commit`之后的提交都会被移除(可以通过git reflog找回)
