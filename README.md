# Synchronizing a Forked Repository with the Original One
A brief guidance about syncing a forked repository with the original one.


Let's say you've forked a repository from ```https://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM```, where "ORIGINAL-DEV-USERNAME" and "REPO-YOU-FORKED-FROM" are the username of main developer and the original name of the project respectively. Suppose you notice that some changes have been made on the original project, and you want to synchronize your current forked project with the original one. You can do this by the following commands. note that, before doing the following commands you need to install git on your machine. 

## Clone Your Fork on Your Local Machine:
```
git clone https://github.com/YOUR-USERNAME/YOUR-FORKED-REPO.git
```
## Add Remote From The Original Repository in Your Forked Repository:
```
cd into/cloned/fork-repo
git remote add upstream https://github.com/ORIGINAL-DEV-USERNAME/REPO-YOU-FORKED-FROM
git fetch upstream
```
## Update Your Forked Project:
```
git pull upstream maste
```
Here, I've supposed that you want to syncronize the forked project with the master branch of the original one. If you want to pull from another branch, you need to use the target branch name instead of master. 
## Upload Your Updated Repository into Your Github account:
```
git push
```
and then enter your username and password for authentication. 



