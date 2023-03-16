- REWRITING COMMIT HISTORY
- The topics discussed here rewrite the commit history
**This should be done with caution**
- General rule: Do not rewrite history that has been shared with others
- if no one other is using the branch you can safely rebase it.
- there is two type of rebase
  1. Rebase : move commits to a new parent or 'base'. ![[rebase-a.png]]
  2. interactive Rebase
- no need for merge commit and you can always do fast-forward merge which keep the history linear
## REBASING PROS AND CONS
### Pros:
- You can incorporate changes from the parent branch
	- You can use the new features/bugfixes
	- Tests are on more current code
	- It makes the eventual merge into master fast-forwardable
- Avoids "unnecessary" commits
	- It allows you to shape/define clean commit histories
### Cons:
- Merge conflicts may need to be resolved
- It can cause problems if your commits have been shared
- You are not preserving the commit history
## Executing a rebase
![[rebase-b.png]]

#git #github 