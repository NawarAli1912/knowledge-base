[[What is Version Control]]
## CheatSheet
![[github-git-cheat-sheet.pdf]]
## Fundamentals
- The working tree (or working directory) is the place where you edit, create, and delete your files. It is the directory that contains all the files and folders that you add to the Git repository, except the `.git` folder, which is not part of the working tree.
  </br>
- The index (or staging area) is a temporary staging area that holds the files that you want to commit. The index is a single binary file that lists all the files in the current branch, their checksums, timestamps, and file names. The index is not another copy of your files, but a pointer to them.
  </br>
- The repository is the place where Git stores the history of your project and the snapshots of your files. The repository is located in the `.git` folder, and it contains all the branches, tags, commits, and other metadata that Git uses to manage your project. The repository is the source of truth for your project, and it is what you push and pull to and from remote servers.
  </br>
- You can link your local repository to a remote one, such as GitHub, GitLab, Bitbucket, or any other server that supports Git, by using the `git remote` command. This way, you can collaborate with other developers, backup your work, and access your project from anywhere.
  </br>
## stashes:
A stash is a way of saving your local changes temporarily without committing them. You can use stashes when you need to switch branches or work on something else, and then come back to your changes later.
- To create a stash, use `git stash` or `git stash push`. This will save your current working directory and index state, and revert them to match the `HEAD` commit. You can also specify a message or include untracked files with options.
  </br>
- To see a list of your stashes, use `git stash list`. This will show you the branch and commit that you created the stash from, and an optional message if you provided one.
  </br>
- To apply a stash, use `git stash apply` or `git stash pop`. The `apply` command will restore your stashed changes to your working directory and index, but keep the stash in the list. The `pop` command will do the same, but also remove the stash from the list. You can specify which stash to apply or pop by using its index or name.
  </br>
- To delete a stash, use `git stash drop`. This will remove the stash from the list. You can specify which stash to drop by using its index or name.
  </br>

## Basic commands
- syntax
  ``` bash
  git [command] <--flag(s)> <argument(s)>
  //
  git help [command]
  // concice help
  git <command> -h
  ```
- configuration
  ``` bash
  git config --global user.email ""
  git config --global user.name ""
  git config --list
  ```
- initialize local git repo
  ``` bash
  git init
  ```
- staging area
  ``` bash
  git add <file> // add to staging area
  git add . // add all to staging area
  git rest <filename> // remove from staging area
  git rest . // remove all from staging area
  ```
- check status of working tree
  ``` bash
  git status
  ```
- commit changes in index
  ``` bash
  git commit
  ```
- push to remote repo 
  ``` bash
  git push
  ```
- pull latest from remote repo
  ``` bash
  git pull
  ```
- clone repository into a new directory
  ``` bash
  git clone
  ```
- Git reset is a command that allows you to move the current branch head to a previous commit and optionally update the index and the working tree. You can use different modes to specify how much you want to undo, such as --soft, --mixed or --hard. For example, if you want to undo the last commit on your wrong branch and keep the changes in your working tree, you can use: 
  ``` bash 
  git reset --soft HEAD~1
  ```
  If you want to discard the changes as well, you can use
  ``` bash
  git reset --hard HEAD~1
  ```
---
# scenario 1:
you  have do some changes and then commit them on a wrong branch what should 
you do, there is 2 choices:
1. One way is to use **git cherry-pick** to copy the commit to the correct branch and then use **git reset --hard** to remove it from the wrong branch.
2. Another way is to use **git reset** to roll back the commits on the wrong branch and then switch to the correct branch.
# scenario 2:
switch branch when there is some changes:
If you have staged or committed your changes, then Git will switch to the other branch without any problem, and your changes will be preserved in the original branch. However, if you have not staged or committed your changes, then Git will not let you switch to the other branch, unless you use the `--force` option or the `-m` option. The `--force` option will discard your changes and switch to the other branch, while the `-m` option will stash your changes and switch to the other branch. You can then use the `git stash pop` command to restore your changes when you switch back to the original branch.

---
#git #github

#git #github 


---
#git #github 
# scenario 3: 
we add modified file a and then stage this file after that we modified it again and during the development process if we see the status of the file we can observe that the first modification of the file is saved in the staging area and the other modification is still in the working tree that's give as a lot of flexibility.