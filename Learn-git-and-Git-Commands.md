### Introduction of git

Git is version control system for tracking changes in computer files and coordinating work on those files among multiple people.

Git is free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows.

### Create

`$ git init`
###### Create a new local repository.

The `git init` command creates a new Git repository. It can be used to convert an existing, unversioned project to a Git repository or initialize a new, empty repository. Most other Git commands are not available outside of an initialized repository, so this is usually the first command you'll run in a new project.

`$ git clone <url>`
###### Clone an existing repository.

`git clone` is a Git command line utility which is used to target an existing repository and create a clone, or copy of target repository. Cloning a local or remote repository. Clone a bare repository. Using shallow options to partially clone repositories. Git URL syntax and supported protocols.

### Local Changes

`$ git status`
##### Changes files in your working directory.

The `git status` command displays the state of the working directory and the stating area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git. Status output does not show you any information regarding the committed project history.

`$ git diff`
##### Changes to tracked files.

`git diff` is a multi-use Git command that when executed runs a diff function on Git data sources. These data sources can be commits, branches, files and more. The `git diff` command is often used along with `git status` and `git log` to analyze the current state of a Git repo.

`$ git diff <filename|filepath>`

Show are list out the change of specific file as per comparison to previous commit.

`$ git add . | $ git add ..`
##### Add all current changes to the next commit.

This command updates the index using the current content found in the working tree, to prepare the content staged for the next commit. It typically adds the current content of existing paths as a whole, but with some options it can also be used to add content with only part of the changes made to the working tree files applied, or remove paths that do not exist in the working tree anymore.

The "index" holds a snapshots of content of the working tree, and it is the snapshot that is taken as the contents of the next commit. Thus after making any changes to the working tree, and before running the commit command, you must use the add command to add any new or modified files to the index.

This command can be performed multiple times before a commit. It only adds the content of the specified file(s) at the time the add command is run; if you want to subsequent changes included in the next commit, then you must run `git add` again to add the new content to the index.

The `git status` command can be used to obtain a summary of which files have changes that are staged for the next commit.

The `git add` command will not add ignored files by default. If any ignored files were explicitly specified on the command line, `git add` will fail with a list of ignored files. Ignored files reached by directory recursion on filename globbing performed by Git (quote your globs before the shell) will be silently ignored. The `git add` command can be used to add ignored files with the -f (force) option.

`$ git add FILENAME`
##### Add particular file changes to the next commit.

`$ git add -p <File>
##### Add some changes in <file> to the next commit.

`$ git commit -m 'Commit message'
##### Add commit message for stagging files (For green colored files)

Use the given <msg> as the commit message. If multiple -m options are given, their values are concatenated as separate paragraphs. The -m option is mutually exclusive with -c, -C, and -F.

`$ git commit -a`

##### Commit all local changes in tracked files.

Tell the command to automatically stage files that have been modified and deleted, but new files you have not told Git about are not affected.

`$ git commit --amend`

##### Change the last commit or revert 

`Don’t amend publish commits.`

`$ git commit --amend -m "an updated commit message"` 

##### Change the last commit or update the last commit message

`Don’t amend publish commits.`

`$ git commit --amend --no-edit`

The --no-edit flag will allow you to make the amendment to your commit without changing its commit message.

`Don’t amend publish commits.`









 
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
`git remote add origin git://git.domain.com:PORT/staging.git`

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