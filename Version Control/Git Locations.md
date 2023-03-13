## Working Tree
- a commit is a single snapshot of a project the working tree is a the location on the local computer that contains the directories and files of a single commit
  </br>
- this is where we can view and edit the files of the project preparing them for the next commit.
  </br>
- checkout a commit is placing it's files and directory into the working tree.
  </br>
## Staging Area/ Index
- the staging area is a list of files and directory that are planed to be included in the next commit.
  </br>
## Local Repository
- contains all the commits that have been made for the project.
- this commits represent the version history of the project.
  <br>
## Remote Repository
- contains the commit of the project on a remote computer.
- the source of truth. 
- integrates with other systems issue trackers and [[Continuous Delivery]] pipeline.
- A remote repository is often a "bare" repository because no body works with this repo locally there is usually no working tree or staging area.
- by convention remote repos names end with ".git".
- git init --bare is called to create the remote repository.
  
  </br>
## Project Directory
contains all of 
- [[#Working Tree]]
- [[#Staging Area/ Index]]
- [[#Local Repository]]


![[git-locations.png]]

#git #github 