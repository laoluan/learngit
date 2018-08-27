$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"

$ mkdir learngit
$ cd learngit
$ pwd

$ git init #在文件夹中初始化Git仓库

$ git add readme.txt

$ git commit -m "wrote a readme file" #提交

$ git status

$ git diff readme.txt #查看文件改动

$ git log #用git log可以查看提交历史，以便确定要回退到哪个版本

$ git reset --hard HEAD^ 或者 --hard <版本号> 或者 --hard HEAD~ 1

$ git reflog #用git reflog查看命令历史，以便确定要回到未来的哪个版本。