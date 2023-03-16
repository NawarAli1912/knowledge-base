the set of commits that trace back to the project's first commit
![[branches-a.png]]
<span style="color:red">NOTE</span> a and b are belong to both branches.
## Benefits of Branches:
- Fast and easy to create.
- Enable experimentation.
- team members can isolate there work branches are not aware of each other.
- enable team development.
- support multiple project versions : you can update each version independently.
- ![[branches-b.png]]
## basics:
- viewing local repository branches :
``` bash
git branch [-a] // -a can be used to see local and remote tracking branches
```
- creating a branch :
``` bash
git branch <name>
```
	simply just create a new branch label reference.
- updates the HEAD reference:
``` bash
git checkout <branch_name_or_commit>
```
	maninly do 2 things:
	1. updatess the HEAD reference to the tip of the new branch
	2. updates the working tree with the new commit files 
	it can be used to checkout a branch or commit.
	compaining checkout with creating new branch.
``` bash
git checkout -b <new-branch>
```
checking out a previous commit lead to a detached head.
basically it means that the head reference is detached from a branch label. 
![[branch-c-detached-head.png]]
create a branch to fix detached head state.
![[branch-d-fixing-detached-head.png]]
- deleting a branch label
``` bash
git branch -d <branch_name>
```
topic branch labels are commonly deleted after the branch is merged.

if you want to delete a branch with unmerged work git will not let you do that.
to delete the branch with it's work 
``` bash
git branch -D <branch_name>
```
it delete the branch but keep the commits as dangling commits so if you accidentally delete a branch you can save your work 
use 
``` bash
git reflog
```
![[branch-e-undoing-an-accidental-branch-delete.png]]

## Tracking branch
Local branches that represent remote branches
Named < remote>/< branch>, for example origin/master
Can become out of synch with local branches
Updated with network commands like clone, fetch, pull
and push
![[tracking-branch-a.png]]
the tracking branch origin/master is denote that on the latest network command the most recent commit was c
### viewing tracking branch names
``` bash
git branch --all
```