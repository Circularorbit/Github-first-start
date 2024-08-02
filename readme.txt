配置用户名

配置邮箱

1. 查看git版本信息
git -v

2. 初始化git本地仓库
git init

3. 查看当前状态
git status

4. 添加文件到暂存区
git add <文件名/通配符>

5. 将暂存区文件提交到版本区
git commit -m '<版本信息>'

6. 将暂存区文件取消
git reset Head <文件名>

7. 查看版本信息
$ git log --pretty=oneline --graph

8. 回退到历史版本
git reset --hard <原来的hash值>

9. 恢复已修改的文件
git checkout -- <文件名>

10. 回退到已回退版本前的版本
git reflog
git reset --hard <原来的hash值>

11. 查看分支
git branch

12. 从当前分支创建分支
git branch <分支名>

13. 删除分支
git branch -d <分支名>

14. 切换分支
git checkout <分支名>

15. 合并分支[合并以后, 被合并的分支依然存在, 且无变化]
git merge <被合并的分支>

16. 设立远程git仓库
git remote add origin https://github.com/Circularorbit/test.git

17. 把分支推送到远程仓库
git push -u origin <分支名>

18. 从远程仓库中复制项目
git clone https://github.com/Circularorbit/test.git

19. 更新远程仓库的代码
git pull origin <分支名>
等价于
git fetch origin <分支名>
git merge origin/<分支名>

20. 合并版本提交信息[注意: 避免合并已经提交到远程仓库的版本]
git rebase Head~数量
git rebase -i <哈希值>

21. rebase合并分支
(子分支)git rebase <主分支名>
(主分支)git merge <子分支>

22. rebase命令版本过程出现的冲突问题解决
(1) 解决冲突
(2) git add .
(3) git rebase --continue

23. 远程代码合并版本
git fetch origin <分支名>
git rebase origin/<分支名>
如果出现文件冲突, 则按照第22点的方式解决

24. 创建tag里程碑版本号
git tag -a <tagName> -m <commitId>

25. 推送本地tag号到远程仓库
git push origin <tagName>

26. 一次性推送本地tag号到远程仓库
git push origin --tags

27. 查看本地tag的详细信息
git show <tagName>

27. 查看本地所有的tag
git tag

28. 查看远程所有的tag
git ls-remote --tags origin

29. 删除tag
git tag -d <tagName>

30. 删除远程仓库tag
git push origin :refs/tags/<tagName>
