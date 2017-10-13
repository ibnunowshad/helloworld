#### Useful common commands for everyone reference here.

1. `git config`  
Sets configuration values for your user name, email, gpg key, preferred diff algorithm, file formats and more. Example:  
`git config --global user.name "jhon"`  
`git config --global user.email "jhon@gmail.com"`

2. `git init`  
Initializes a git repository - creates the initial ‘.git’ directory in a new or in an existing project. Example:  
`cd /home/user/my_new_git_folder/`  
`git init`

3. `git clone`  
Makes a Git repository copy from a remote source. Also adds the original location as a remote so you can fetch from it again and push to it if you have permissions. Example:  
`git clone git@github.com:user/test.git`

4. `git add`  
Adds files changes in your working directory to your index. Example:  
`git add .`

5. `git rm`  
Removes files from your index and your working directory so they will not be tracked. Example:  
`git rm filename`

6. `git commit`  
Takes all of the changes written in the index, creates a new commit object pointing to it and sets the branch to point to that new commit. Examples:  
`git commit -m "committing added changes"` 

7. `git status`
Shows you the status of files in the index versus the working directory. It will list out files that are untracked (only in your working directory), modified (tracked but not yet updated in your index), and staged (added to your index and ready for committing). Example:  
`git status`

8. `git branch`  
Lists existing branches, including remote branches if ‘-a’ is provided. Creates a new branch if a branch name is provided. Example:  
`git branch` shows local branches only  
`git branch -a` shows local and remote branches    
`git branch feature1` create local branch  

9. `git checkout`
Checks out a different branch - switches branches by updating the index, working tree, and HEAD to reflect the chosen branch. Example:  
`git checkout feature1`

10. `git merge`  
Merges one or more branches into your current branch and automatically creates a new commit if there are no conflicts. Example:  
`git merge feature1`

11. `git reset`  
Resets your index and working directory to the state of your last commit. Example:  
`git reset --hard HEAD`

12. `git stash`  
Temporarily saves changes that you don’t want to commit immediately. You can apply the changes later. Example:  
`git stash`  
`git stash apply` to restore them  

13. `git tag`  
Tags a specific commit with a simple, human readable handle that never moves. Example:  
`git tag -a v1.0 -m 'this is version 1.0 tag'` [Refer here for more details](git-tips)

14. `git fetch`  
Fetches all the objects from the remote repository that are not present in the local one. Example:  
`git fetch origin dev`

15. `git pull`  
Fetches the files from the remote repository and merges it with your local one. This command is equal to the git fetch and the git merge sequence. Example:  
`git pull origin dev`

16. `git push`  
Pushes all the modified local objects to the remote repository and advances its branches. Example:  
`git push origin master`

17. `git remote`  
Shows all the remote versions of your repository. Example:  
`git remote add origin git://git.tusisobar.com:PORT/staging.git`

18. `git log`  
Shows a listing of commits on a branch including the corresponding details.

19. `git show`  
Shows information about a git object.

20. `git ls-tree`  
Shows a tree object, including the mode and the name of each item and the SHA-1 value of the blob or the tree that it points to. Example:  
`git ls-tree dev`

21. `git cat-file`  
Used to view the type of an object through the SHA-1 value. Example:  
`git cat-file -t e69de29bb2d1d6434b8b29ae775ad8c2e48c5391`

22. `git grep`  
Lets you search through your trees of content for words and phrases. Example:   
`git grep "controller_"` search everything in the repo  
`git grep "controller_" -- *.php` search specific files with php ext in the repo 

23. `git diff`  
Generates patch files or statistics of differences between paths or files in your git repository, or your index or your working directory.

24. `git gui`  
Graphical tool to push/commit.

24. `gitk`  
Graphical Tcl/Tk based interface to a local Git repository.

25. `git archive`  
Creates a tar or zip file including the contents of a single tree from your repository. Example:  
`git archive --format=zip master^ README >files.zip` Add only README file to the zip from master branch  
`git archive --format=zip master^ >files.zip` Add everything to the zip from master branch

26. `git gc`  
Garbage collector for your repository. Optimizes your repository. Should be run occasionally.

27. `git fsck`  
Does an integrity check of the Git file system, identifying corrupted objects.

28. `git prune`  
Removes objects that are no longer pointed to by any object in any reachable branch.

29. `git commit -S -m "signed commit msg"`  
Push signed commits.