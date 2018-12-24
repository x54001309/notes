# git笔记

1. git clone 克隆仓库
2. git log 查看提交记录
3. git log --graph --online branch_name branch2_name 比较两个分支的提交记录
4. git diff old_id new_id 比较两次提交的差别
5. git diff 比较本地文件和暂存区文件
6. git diff --staged 比较暂存区文件和仓库中最新的commit
7. git checkout commit_id/branch_name 检出指定ID/分支版本
8. git checkout -b new_branch_name 等于git branch new_branch_name, git checkout new_branch_name
9. git add file_name 提交文件到暂存区
10. git reset file_name 将文件从暂存区移除(不准备提交该文件)
11. git reset --hard 将本地文件和暂存区文件恢复成最新一次提交的状态
12. git commit -m "注释" 提交暂存区中的文件到本地仓库
13. git branch 列出当前所有分支
14. git branch branch_name 新建指定名字的分支
15. git branch -d branch_name 删除指定名字的分支
16. git branch -a 列出包含远程分支在内的所有分支
17. git merge branch_name 合并branch_name到当前分支
18. git merge --abort 将文件恢复到你开始合并之前的状态
19. git remote 查看远程分支
20. git remote -v 查看远程分支详细信息
21. git remote add origin http://xxxx.git 添加远程分支，origin为远程仓库别名，url为远程分支路径
22. git push origin master 将本地master分支推送到远程master分支上，其中origin为远程仓库别名
23. git pull origin master 将远程master分支拉取到本地master分支上，其中origin为远程仓库别名
24. git pull origin remote_branch:local_branch 将指定远程分支remote_branch拉取到指定本地分支local_branch
25. git fetch origin 更新origin对应的所有本地分支