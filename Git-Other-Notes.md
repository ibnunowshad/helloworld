Download the puttygen.exe file and generate the public and private key.  And export it. 
And then copy and paste it in C:\Users\Habeeb\.ssh 
We have save the file as id_rsa – private and  id_rsa_pub   - public. 

GIT TUTORIAL:
 - https://www.kernel.org/pub/software/scm/git/docs/gittutorial.html

First go to the folder and then initiate git
- `cd /path/to/folder`

### Git Initiate
`git init 
git config --global user.name "john"
git config --global user.email "john@gmail.com"
git remote add origin ssh://git@git.domain.com:5214/folder/project.git
git pull origin master`  --> first pull from remote

### Branch
- `git branch develop`  - create new branch
- `git checkout develop`  - swithed to branch 'develop'
- `git gui`
- `git status` - look for the status of the commits`


### To check the changes
- `git diff`

### PULL DATA:
- `git pull origin dev`  - pull data from the git server ie From ssh://git@git.domain.com:5214/folder/project.git

### PUSH DATA: - THIS comment will push data to specified branch (develop)
`git add .
git commit -m "changed file data"    
git push origin develop`    

TO REMOVE THE GIT AND THEN YOU CAN INITIATE AGAIN 
- `rm -rf .git`

### To reset the local branch if confilcts happen. 
`git fetch --all
git reset --hard origin/dev` 

after reset push data 
`git add .
git commit -m "changed file data"    
git push origin dev`

This below code to set false if we get some replacing issue.
- `git config core.autocrlf false`

### Merge Branch:
`git checkout uat
git merge dev
git push origin uat`

### Delete a remote branch
 - `git push origin --delete <branch>` # Git version 1.7.0 or newer 
 - `git push origin :<branch>` # Git versions older than 1.7.0

### Delete a local branch
 - `git branch --delete <branch>`
 - `git branch -d <branch>` # Shorter version
 - `git branch -D <branch>` # Force delete un-merged branches

### Delete a local remote-tracking branch
 - `git branch --delete --remotes <remote>/<branch>`
 - `git branch -dr <remote>/<branch>` # Shorter
 - `git fetch <remote> --prune` # Delete multiple obsolete tracking branches
 - `git fetch <remote> -p` # Shorter


### Create a new repository

`git clone ssh://git@git.domain.com:5214/folder/project.git
cd project folder
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master`

### Existing folder

`cd existing_folder
git init
git remote add origin ssh://git@git.domain.com:5214/folder/project.git
git add .
git commit
git push -u origin master`

### Existing Git repository

`cd existing_repo
git remote add origin ssh://git@git.domain.com:5214/folder/project.git
git push -u origin --all
git push -u origin --tags`

### move to a scratch dir
Copy / Duplicating git repo from one repository to another:
`mkdir foo; cd foo` 

### Make a bare clone of the repository
`git clone --bare https://github.com/exampleuser/old-repository.git`

### Mirror-push to the new repository
- `cd old-repository.git`
- `git push --mirror https://github.com/exampleuser/new-repository.git`

### Remove our temporary local repository
- `cd ..`
- `rm -rf old-repository.git ` 
