A stash is a way of saving your local changes temporarily without committing them. You can use stashes when you need to switch branches or work on something else, and then come back to your changes later.
- To create a stash, use `git stash` or `git stash push`. This will save your current working directory and index state, and revert them to match the `HEAD` commit. You can also specify a message or include untracked files with options.
  </br>
- To see a list of your stashes, use `git stash list`. This will show you the branch and commit that you created the stash from, and an optional message if you provided one.
  </br>
- To apply a stash, use `git stash apply` or `git stash pop`. The `apply` command will restore your stashed changes to your working directory and index, but keep the stash in the list. The `pop` command will do the same, but also remove the stash from the list. You can specify which stash to apply or pop by using its index or name.
  </br>
- To delete a stash, use `git stash drop`. This will remove the stash from the list. You can specify which stash to drop by using its index or name.
  </br>


#git #github 