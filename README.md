# Testing Automation Course


## Learn basics of git

git init    -  inicijalizuje git repozitorijum u nekom direktorijumu

### Clonning repository
git clone username@host:/path/to/repository

### status
git status

### Configure name and email
git config --global user.name "Sam Smith"     
git config --global user.email sam@example.com    

### Add file to git to start tracking it's chnages
git add <filename>
git add *

### Commi to ocal repository. Changes are still not on the server
git commit -m "Commit message"
git commit
git commit -a

### vi   - editor
When 'vi' editor opens, press 'i' in order to start changing the file
when done, press ESC and then :wq   (write - quit)

### push changes to server
git push origin master


### If local repository is not connected with main repo, add server to which all changes will be pushed
git remote add origin <server>

### list repos
git remote -v

### create new branch and jump on it
git checkout -b <branchname>

### change branch
git checkout <branchname>

### list branches
git branch

### delete branch
git branch -d <branchname>
>> $ git branch -d feature/login

### push branch to server
git push origin <branchname>

### push all branches to server
git push --all origin

### delete branch on server
git push origin :<branchname>
>> git push origin --delete feature/login

### take all changes from server
git pull

### merge branches
git merge <branchname>

# when there are conflicts - check conflicts in base file - check changes before merge
git diff
git diff --base <filename>
git diff <sourcebranch> <targetbranch>

# when you resolve conflicts
git add <filename>

# when all conflicts are resolved
git commit

# last 10 commits
git log

