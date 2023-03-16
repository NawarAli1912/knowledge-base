Merging combines of independent branches.
![[merging_a.png]]
## Types:
1. Fast-forward merge
   ![[fast_forward_merge(ff).png]]
   it is only possible if no other commit have been made to the base branch since branching.
   ![[fast_forward_merge(ff)_b.png]]
   git will always try to perform fast-forward merge unless you tell not to.
   the resulting commit history of using ff is linear.
2. Merge commit
   ![[merge_commit_a.png]]
   it's easier to see the branches in the resulting commit history
   the steps of performing a merge commit is the same as fast-forward merge
   if the fast-forward merge is not possible then merge commit will be used.
   ![[merge_commit_b.png]]
1. Squash merge
2. Rebase