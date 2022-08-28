## Lesson 2

### 1. Basics
```bash
# initialize a git repo
git init

# stage and commit
git add .
git add *.js && git commit -m 'initial commit'

# clone an existing repo
git clone [url]

# check status of your files
git status

# check what you've changed but not yet staged
git diff

# compare staged changes to your last commit
git diff --staged

# skipping staging area, i.e. add and commit in one go
git commit -a -m 'updated lesson2.md'
```
