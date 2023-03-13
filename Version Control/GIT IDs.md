- a git id is the name of a [[GIT Objects]].
- all of the object stored by git are named with a 40-character hexadecimal string.
- also known as object id, SHA-1, hash and checksum.
- use SHA-1 of the file content to get a git id:
``` bash
git hash-object <file>
```
## shortened git ids
``` bash
git log --oneline
```
will return only the first 7 characters of the commits ids
## view the content of an object
``` bash
git show <object-id>
```
we can use a [[#shortened git ids]]

#git #github