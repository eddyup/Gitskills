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

## 利用标签回退修补bug

总结一下，通过标签修改bug的步骤如下：

- 主分支回退到打标签的那次提交
- 拉取分支bugfix
- 主分支立即回到最新状态
- 切换到bugfix分支，修改bug，发版本，打新标签
- 合并bugfix分支到主干上
- 手动推送标签到远程

否则直接回退在master分枝上修复bug，然后会提交不到远程仓库（例如 GitHub）中去，因为远程仓库比新的库要新。

=====
方法：

可以先使用 git checkout tagname, 将HEAD指向tagname，然后 git checkout -b bugFix 建立新的分支，修复bug，然后 git checkout master，此时回到的是master最新的状态，然后 merge 就可以了；需要注意的是此时需要对比修改。

git checkout tagname 和 git reset --hard tagname 都可以回退到历史版本，但是第一种是改变 HEAD 的指向，回到 master 分支之后还是指向最新的节点。但是 reset 不一样，直接将 当前工作区域重置到 tagname 的版本。

## 可视化软件
Fork
Sublime git

## Website

[Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

[LearnGitBranching](https://learngitbranching.js.org/)

