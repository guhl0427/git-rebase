# git-rebase

## git rebase xxx

将当前分支变基到xxx分支，变基的过程中，需要处理每一次冲突，处理完成冲突后，需要添加到暂存区`git add .`，之后`git rebase --continue`进行下一次的冲突处理。

## git rebase -i xxx 合并提交

### 作用
合并提交。日常开发中，往往会将一些与功能本身没有太多关系的代码提交，如果不进行提交合并的话，这些没有意义的提交上生产后会被带入主分支，不优雅。那么此时就可以合并提交，展示一个清晰合理的提交历史。

### 命令
git rebase -i commit-hash

将commit-hash值之后的commit合并为同一个commit

git rebase -i HEAD~4

将前4个commit合并为同一个commit

### 操作流程
1. git rebase -i commit-hash
2. 按`i键`进入编辑模式
3. 将最上面的一次提交设置为`pick`，其他的提交设置为`squash`。
4. 按`ESC键`然后输出`:wq`，保存并退出
5. 在之后出现的编辑页面继续按`i键`进入编辑模式，整理`commit信息`（不需要的直接删除就行dd快速删除行）

# commit test

main commit1
main commit2
main commit3

dev commit1
dev commit2
dev commit3

# fix
丢弃掉那段历史吧

commit1
commit2
commit3
commit4
commit5
commit6