# Testing Automation Course

## Basic and everyday Git commands

Think in terms of workflow steps.

## Setup & configuration

```
git config --global user.name "Nenad"
git config --global user.email "you@example.com"

git config --global core.autocrlf input   # good default on macOS/Linux
git config --global core.autocrlf true    # often used on Windows
```

## Creating / cloning repos
```
git init                        # start new repo in current folder
git clone <url>                 # clone existing repo
git clone git@github.com:user/repo.git
```

## Everyday workflow

```
git status                      # see changes & branch
git add <file>                  # stage specific file
git add .                       # stage all tracked + new files
git commit -m "Describe change" # create commit

git log --oneline --graph --all # nice history view
git diff                        # see unstaged changes
git diff --staged               # see staged changes
```

## Branching & merging

```
git branch                      # list branches
git branch feature/login-tests  # create branch

git checkout feature/login-tests    # switch (older syntax)
git switch feature/login-tests      # modern syntax

git merge feature/login-tests   # merge into current branch
git branch -d feature/login-tests   # delete merged branch
```

## Sync with remote

```
git remote -v                   # list remotes
git pull                        # fetch + merge from remote
git fetch                       # fetch only
git push                        # push current branch
git push -u origin feature/login-tests  # push new branch and set upstream
```

## Undo & cleanup (most common)

```
git restore <file>              # discard local changes (not staged)
git restore --staged <file>     # unstage

git reset --hard HEAD~1         # remove last commit (dangerous if pushed)
git revert <commit-hash>        # new commit that undoes previous one
```

For daily work as a test engineer, mastering these is enough 90% of the time.



# Additional git commands

```
git init    -  inicijalizuje git repozitorijum u nekom direktorijumu
```

### Clonning repository

```
git clone username@host:/path/to/repository
```

### status
```
git status
git status -s
git status --short
git status --branch

```

### last 10 commits
```
git log
git log --oneline -10
git log --oneline --graph --all        # see history
```

### Configure name and email
```
git config --global user.name "Sam Smith"
git config --global user.email sam@example.com
git config --global core.autocrlf input       # for macOS/Linux
git config --global core.autocrlf true        # for Windows
git config --list
git config --global --edit
git config --system --edit
git config --local --edit
```

### Add file to git to start tracking it's chnages
```
git add <filename>
git add .
```

### Commi to local repository. Changes are still not on the server
```
git commit -m "Commit message"
git commit
git commit -a
git commit --verbose                   # show diff of changes included
git commit -a -m "Merge branch 'feature/login' into 'master'"
git commit -m "Resolved merge conflicts"
git commit --amend -m "New commit message"   # change last commit message
git commit --amend                      # change last commit message in editor
```

### vi   - editor
When 'vi' editor opens, press 'i' in order to start changing the file
when done, press ESC and then :wq   (write - quit)

### push changes to server
```
git push origin master
```


### If local repository is not connected with main repo, add server to which all changes will be pushed
```
git remote add origin <server>
```

### list repos
```
git remote -v
```

### create new branch and jump on it
```
git checkout -b <branchname>
git switch -c <branchname>
>> $ git checkout -b feature/login
>> $ git switch -c feature/login
```

### change branch
```
git checkout <branchname>
git switch <branchname>
```

### list branches
```
git branch
git branch -a        # all branches, including remote
git branch -r        # remote branches only
git show-branch
git show-branch --all
```

### delete branch
```
git branch -d <branchname>
>> $ git branch -d feature/login
git branch -D <branchname>   # force delete
```

### push branch to server
```
git push origin <branchname>
```

### push all branches to server
```
git push --all origin
```

### delete branch on server
```
git push origin :<branchname>
>> git push origin --delete feature/login
```

### take all changes from server
```
git pull
```

### merge branches
```
git merge <branchname>
>> git merge feature/login
```

## Resolving conflicts

### when there are conflicts - check conflicts in base file - check changes before merge
```
git diff
git diff --base <filename>
git diff <sourcebranch> <targetbranch>
```

### when you resolve conflicts
```
git add <filename>
```

### when all conflicts are resolved
```
git commit
```





