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
