# Gitskills
Learn how to use git.

MIT license.

##SSH key

ssh-keygen -t rsa -C "youremail@example.com"

## git command

### git config
 git config --global user.name "Your Name"

 git config --global user.email "email@example.com"

## git cheat:

### Initional
git init

### Add and commit files
git add filename

git add filename1, filename2

git add .


git commit -m "message"

### See status

git status

git diff file

### See log
git log

git log --pretty=oneline

git reflog

### version change
git reset --hard commit-id

git reset --hard tag

git revert commit-id

### discard changes
git checkout --file

git reset HEAD file

git rm file, git commit -m "message"

### branch
git branch

git branch branchname

git checkout -b branchname

git checkout branchname

git merge branchname

git merge --no-ff -m "message"

git branch -d branchname

git log --graph

git log --graph --pretty=oneline --abbrev-commit

### tag
git tag

git tag v1.0

git tag v1.0 commit-id

git tag -d v1.0

### Remote 

git push origin master

git pull origin master


## Website

[Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

[LearnGitBranching](https://learngitbranching.js.org/)

