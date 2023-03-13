## Branches
- master is the default name of the main branch in the repository
- a branch is an independent path for a set of commits
- if we never create a branch in a repository then by default all commits are part of the master branch.
- a branch label points to the most recent commit in the branch 
	- the tip of the branch
	- implemented as a [[GIT References]]
	- ![[branch-tip.png]]
		- all the previous 3 commit belong to the master branch in the other hand master label point to the tip of the branch.
	- branches in git implemented using tiny branch label so branches are extremally simple to implement and use few resources.
## Head
- is a reference to the current commit. 
- usually points to the branch label of the current branch.
- One Head per repository
- implemented as [[GIT References]] we can view the content in .git/HEAD
### Referencing prior commits with ~ and ^
- ~ or ~1 = parent
- ~ 2 or ~~ = parent's parent
- ^ refers to a parent in  a merge commit (^parentnum)
- so ^ with a number is different of using multiple ^
- ![[git-caret-tilda.png]]
  refers to the parent's second parent
- so Tilda and Caret can be combined to refers to any commit.
### Tags
- Reference/label attached to a specific commit
- there are two types:
	- Lightweight a simple reference to commit much like a branch label or head
	- Annotated tag one of the 4 [[GIT Objects]] includes meta data about the commit. recommended
- viewing and using tags
``` bash
git tag [-a] // -a annotated tag
```
