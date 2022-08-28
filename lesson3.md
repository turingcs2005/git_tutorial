## Lesson 3: Branching

### 1. create a new branch
```bash
# display current branches
git branch

# create a pointer at the same commit you are currently on without changing branch
git branch [branch name]

# create a branch off your current branch and check it
git checkout -b [branch name]

# create a branch off a remote branch and check it out
git checkout -b [branch name] [remote repo name]/[remote branch name]
```

### 2. check out, merge, display branch info., delte remote branch, etc.

```bash
# check out an existing branch
git checkout [branch name]

# merge current branch with target branch
git merge [target branch name]

# delete a merged branch
git branch -d [branch name]

# delete a branch that has not yet been merged to your current branch
git branch -D [branch name]

# display all branches already merged to your current branch
git branch --merged

# display all branches not yet merged to your current branch
git branch --no-merged

# create a local branch (branch name will be the same as the remote branch name) to track a remote branch
git checkout --track [remote repo name]/[remote branch name]

# display all tracking branches and what remote repos/branches they are tracking
git branch -vv

# delete a remote branch
git push [remote repo name] --delete [remote branch name]
```

### 3. rebasing
1. Rebasing takes all the changes that were commited on one branch and replay them on another one.
2. Rebasing produces cleaner (linear) git history. 
3. Rebasing rewrites commit history. 
Scenario:  you are working on an experiment (feature) branch, and your colleageus pushed changes to master branch. Rebase experiment branch.
```bash
# rebase branch experiemnt to branch master
git checkout experiment
git rebase master
```
<mark>Do not rebase commits used by other developers</mark> (outside your repo), because they may have already created commits off your (unrebased) commits.