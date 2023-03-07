## commands:
- To change directory:
```sh
cd [Absolute path] | [relative path]
```
- to go to parent folder:
```sh
cd ..
```
- to make a new directory:
```sh
mkdir [directory name]
```
- ### cat command :
	1. Displaying the contents of a file: This is probably the most common use of `cat`.
	2. Concatenating files: The name "cat" actually comes from "concatenate", which means to join together. When used with multiple file names as arguments, `cat` will join the files together and display the resulting content on the console. For example, `cat file1.txt file2.txt` will display the contents of "file1.txt" followed by the contents of "file2.txt".
	3. Recording user input: Another use of `cat` is to record user input into a file. This is typically done using the "here-document" syntax. For example, `cat > file.txt` will start recording user input into "file.txt", and the recording will continue until the user types Ctrl+D to signal the end of input.
    4. Piping input to another command: `cat` can also be used in a pipeline to pass the contents of a file or multiple files to another command. For example, `cat file.txt | grep "hello"` will pass the contents of "file.txt" to the `grep` command, which will search for lines that contain the string "hello".

---
## Redirection:
the basic work flow of any linux command is that it takes an input and gives an output.
the standard input device is the keyboard.
the standard output device is the screen.
1. 0 is for standard input.
2. 1 is for standard output.
3. 2 is for standard error.
we can change the standard input and/or output using **Redirection**

## Piping:
we can pass the output of a command to be the input of another command 
```sh
command1 | command2
```

## Resources:
[CheatSheet](https://devhints.io/bash)
[grep CheatSheet](https://devhints.io/grep)
[bash CheatSheet](https://cheatography.com/jluis/cheat-sheets/bash-and-unix-commands/)
[vim CheatSheet](https://vim.rtorr.com/)

---
## Related:
[[Absolute vs relative path]]
#shell #command_line #bash