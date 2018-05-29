# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files 
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > * show current working directory path
> > ```
> > pwd
> > ```
> > * creating a directory
> > ```
> > mkdir new_directory
> > ```
> > * deleting a directory (empty directory)
> > ```
> > rmdir directory_name
> > ```
> > * deleting a directory (including all the  
> > files inside the directory)
> > ```
> > rm -r directory_name
> > ```
> > * creating a file using `touch` command
> > ```
> > touch file_name
> > ```
> > * deleting a file
> > ```
> > rm file_name
> > ```
> > * renaming a file
> > ```
> > mv old_file new_file
> > ```
> > * listing hidden files 
> > ```
> > ls -ld .* | grep '^[^d]'
> > ```
> > * copying a file from one directory to another
> > ```
> > cp dir1/file_name dir2
> > ```
> > * show file content
> > ```
> > less file_name
> > ```
> > * show file name of a given path
> > ```
> > basename path_name
> > ```


---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > `ls` list all the files and directories in the current directory. Hidden files or direcgtories are not shown.  
> > `ls -a` list all the files and directories, including all the hidden directoris and files (whose names begin with a dot.)  
> > `ls -l` list all the visible files and directories in long format, including information on file permission, size, owner, time of last modification and etc.  
> > `ls -lh` list all the visible files and directories in long format. Sizes are listed with unit suffixes: B, K, M, G and etc.  
> > `ls -lah` list all the files and directories including the hidden ones in long format and list size with unit suffixes.  
> > `ls -t` list all the files and directories primarily sorted by last modified time (from most recently modified first), secondarily sorted by operand in lexicographical order.  
> > `ls -Glp` list all the files and directories in long format. All the directories has a '/' after the directory name and are shown in color.  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > 1. `ls -1` list each file or directory on a line.
> > 2. `ls -m` separate file/directory names with ','.  
> > 3. `ls -r` list files and directories in reverse order.  
> > 4. `ls -R` list content in the subdirectores as well.  
> > 5. `ls -x` list files/directories by rows 

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` takes input from stdin as the argument for a command. For example, if we would like to check the number of lines in all the .txt files in a directory, we can use 
> > ```
> > ls *.txt | xargs wc -l 
> > ```

 

