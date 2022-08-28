## Lesson 2: The Basics

### 1. initialize, check status, stage and commit, clone
```bash
# initialize a git repo
git init

# stage and commit
git add .
git add *.js && git commit -m 'initial commit'

# skipping staging area, i.e. stage every file and commit in one go
git commit -a -m 'updated lesson2.md'

# check status of your files
git status
```
### 2. check difference
```bash
# check what you've changed but not yet staged
git diff

# compare staged changes to your last commit
git diff --staged

# compare difference between 2 commits
git diff [commit1] [commit2]

```

### 3. remove file and move file
```bash
# remove a previously commited file
git rm [file name]
git commit -m 'removed file'

# move a file
git mv [old file] [new file]

# git mv is equivalent to
# mv [fold file] [new file]
# git rm [old file]
# git add [new file]
```

### 4. git log
```bash
git log

# -p: show difference between commits; -2: limit output to only the last 2 entries
git log -p -2 

# one-line log
git log --pretty=oneline 

# show hash, author, subject plus ASCII graph
git log --pretty=format:"%h %an %s" --graph

# commits since 2 weeks ago
git log --since=2.weeks
# You can use minutes, hours, days, weeks, months, years...
```

### 5. amend last commit
```bash
git commit -m 'forgot to stage a file'
git add [forgotten file]
git commit --amend
# 2nd commit replace the first

```

### 6. unstage a staged file; discard changes; reset to a previous commit
```bash
# unstage a file
git reset HEAD [file name]

# discard changes
git checkout -- [file name]

# reset to previous commit
git reset [previous commit, or HEAD] --hard

```

### 7. working with remotes

```bash
# clone an existing repo
git clone [remote repo url]

# inspect remote
git remote show [remote repo name]

# show all remote repo names
git remote 

# show remote repo names + url
git remote -v

# add a remote repo
git remote add [remote repo name] [remote repo url]

# push current branch to a remote branch (often executed right after 'git remote add...')
git push -u [remote repo url] [remote branch name]

# remove a remote repo
git remote remove [remote repo name]

# rename a remote repo
git remote rename [old remote repo name] [new remote repo name]

# push to remote
git push [remote rempo name] [remote branch name]

# fetch files without merge
git fetch [remote repo name]

# merge current branch with a remote branch 
git merge [remote repo name]/[remote branch name]

# fetch and then merge
git pull [remote repo name] [remote branch name]
```

### 8. tagging
```bash
# create an annotated tag
git tag -a v1.4.1 -m 'version 1.4.1'

# list available tags
git tag

# list tags with pattern 'v1.1.*'
git tag -l 'v1.1.*'

# tag a previous commit
git tag -a [tag] [hash key of a previous commit]

# push all local tags to remote server
git push [remote name] --tags

```