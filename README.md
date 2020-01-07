# Version-Control
GameDev HQ Version Control for Unity

For Msc OS X: Add .DS_Store file to .gitignore

Includes branches and files for:
- master
- dev
- inventory
- quest

Initial git setup on local machine:

git config --global user.email "...@..."
git config --global user.name "..."
git config --list

Repository originates on GitHub:

git clone ...


Repository originates on local machine:

git init
git remote add origin ….

git remote --v
git branch --v

git status
git --help

Push master branch to GitHub repository:

git pull origin master
git add .
git commit -m "initial commit"
git push --set-upstream origin master
git push -u origin master

Create branches on local machine:

git branch dev or git checkout -b dev
git inventory
git branch quest
git branch

Change to new branches, add and merge files from other branches:

git checkout dev
… add file(s)

git checkout inventory
… merge and add file(s)
git merge dev

git checkout quest
… merge and add file(s)
git merge inventory

git checkout dev
git merge quest

Update GitHub repository:

git add .
git commit -m "adds all files to dev branch"
git push origin dev

Push new branches and files to GitHub repository:

git push origin inventory
git push origin quest

Integrate final updates into the master branch:

git checkout master
git pull origin master
git merge dev

Update GitHub repository with the master branch:

git pull origin master
git add .
git commit -m "adds all files to master branch"
git push origin master

Force revert (resets GitHub as well! - recommend using git checkout, instead):

git reset --hard c41eecfe260740001049f2dfde743fda78f59f83

git push --force origin master
