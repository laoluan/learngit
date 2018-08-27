$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"

$ mkdir learngit
$ cd learngit
$ pwd

$ git init #在文件夹中初始化Git仓库

$ git add readme.txt

$ git commit -m "wrote a readme file" #提交

$ git status

$ git diff <readme.txt> #查看用户当前编辑文件跟add之后的区别

$ git diff <readme.txt> --cached #查看add之后的文件跟commit之后的区别

$ git log #用git log可以查看提交历史，以便确定要回退到哪个版本

$ git reset --hard HEAD^ 或者 --hard <版本号> 或者 --hard HEAD~ 1

$ git reflog #用git reflog查看命令历史，以便确定要回到未来的哪个版本。

$ git diff HEAD -- Git命令.md #当前文件和版本库的区别

$ git push origin master #向远程库推送

$ git clone git@github.com:laoluan/gitskills.git #从远程克隆

$ git remote add origin git@github.com:laoluan/gitskills.git #将本地库关联远程库

$ git checkout -b dev #创建dev分支然后切换到dev分支

$ git branch dev #创建dev分支

$ git checkout dev #切换到dev分支

$ git branch #查看当前分支

$ git merge dev #合并dev分支到当前分支

$ git branch -d dev #删除dev分支

$ git log --graph --pretty=oneline --abbrev-commit #查看分支情况

$ git merge --no-ff -m "merged bug fix 101" issue-101 #禁用快进模式合并分支

$ git stash #保存当前工作区

$ git stash pop #恢复工作区并删除status

$ git stash apply #恢复工作区

$ git stash drop #删除status


多人协作的工作模式通常是这样：

首先，可以试图用git push origin <branch-name>推送自己的修改；

如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并；

如果合并有冲突，则解决冲突，并在本地提交；

没有冲突或者解决掉冲突后，再用git push origin <branch-name>推送就能成功！

如果git pull提示no tracking information，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream-to <branch-name> origin/<branch-name>。

这就是多人协作的工作模式，一旦熟悉了，就非常简单。


$ git rebase #变基 把分支变直

$ git tag v0.1 #在当前分支当前位置打标签

$ git tag v0.9 f52c633 #指定commit id打标签

$ git show v0.9 #查看标签

$ git tag -a v0.1 -m "version 0.1 released" 1094adb #打标签并附加说明文字

$ git tag -d v0.1 #删除本地标签

$ git push origin v1.0 #推送标签到远程

$ git push origin --tags #一次性推送全部尚未推送到远程的本地标签

$ git push origin :refs/tags/v0.9 #删除远程标签

$ git remote rm origin #删除/解除远程库关联

关联多个库 git remote add github git@github.com:michaelliao/learngit.git git remote add gitee git@gitee.com:liaoxuefeng/learngit.git

$ git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit" #天机不可泄露