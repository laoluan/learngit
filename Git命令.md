$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"

$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngit

$ git init
Initialized empty Git repository in /Users/michael/learngit/.git/

$ git add readme.txt

$ git commit -m "wrote a readme file"
[master (root-commit) eaadf4e] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt

 $ git status

$ git diff readme.txt 