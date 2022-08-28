## Lesson 2

### 1. initialize, check status, stage and commit, clone
```bash
# initialize a git repo
git init

# stage and commit
git add .
git add *.js && git commit -m 'initial commit'

# skipping staging area, i.e. stage every file and commit in one go
git commit -a -m 'updated lesson2.md'

# clone an existing repo
git clone [url]

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

### 3. remove files
```bash
# after removing a file
git rm [file name]

```
