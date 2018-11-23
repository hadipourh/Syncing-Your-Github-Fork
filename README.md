# Keep your fork synced
A brief guidance about syncing a forked repository with the original one.


Let's say you've forked a repository from `https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY`, where "ORIGINAL_OWNER" and "ORIGINAL_REPOSITORY" are the username of main developer, and the name of original repository respectively. Suppose you want to synchronize your current fork repository with the original one. You can do this by the following commands. note that, before doing the following commands you need set up Git on your machine. 

## Step1: Create a local clone of your fork
```
git clone https://github.com/YOUR-USERNAME/YOUR-FORKED-REPO.git
```
## Step2: Configure Git to sync your fork with the original repository
Add remote from original repository in your forked repository
```
cd into/cloned/fork-repo
git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```
To verify the new upstream repository you've specified for your fork, type `git remote -v` again. You should see the URL for your fork as origin, and the URL for the `original` repository as `upstream`.

Now, you can keep your fork synced with the upstream repository. Before you can sync your fork with an upstream repository, you must configure a remote that points to the upstream repository in Git. Fetch the branches and their respective commits from the upstream repository. Commits to `master` will be stored in a local branch, `upstream/master`.
```
git fetch upstream
```
Check out your fork's local `master` branch.
```
git checkout master
```
## Step3: Update Your Fork:
Merge the changes from `upstream/master` into your local `master` branch. This brings your fork's `master` branch into sync with the upstream repository, without losing your local changes.
```
git pull upstream master
```
Here, I've supposed that you want to syncronize the forked project with the master branch of the original one. If you want to pull from another branch, you need to use the target branch name instead of master. 
## Step4: Upload Your Updated Repository into Your Github account:
```
git push
```
and then enter your username and password for authentication. 

## References
[1] https://help.github.com/articles/syncing-a-fork/



