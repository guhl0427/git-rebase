# git-rebase

## git rebase xxx

将当前分支变基到xxx分支，变基的过程中，需要处理每一次冲突，处理完成冲突后，需要添加到暂存区`git add .`，之后`git rebase --continue`进行下一次的冲突处理。

## git rebase -i xxx

git rebase -i commit-hash

将commit-hash值之后的commit合并为同一个commit

git rebase -i HEAD~4

将前4个commit合并为同一个commit

# commit test

main commit1
main commit2
main commit3

dev commit1
dev commit2
dev commit3
123123
