# Lecture-note for 5th class

### I/O redirection 
#### standard output
By default, standard output is screen of bash.
But we can switch standard output by using ">"
Ex)
```sh
$ ls > newfile.txt
```
If you use this command with a same file repeatly, It is **replaced.**
If you want **add** contents on same file, you can use a command ">>"
Ex)
```sh
$ ls > newfile.txt
$ ls -lh >> newfile.txt
```
#### standard input
By default, standard input is from keyboard.
But we can redirect standard input by using "<"
Ex)
```sh
$ sort < newfile.txt
```
And you can mix commands "<" and ">"
Ex)
```sh
$ sort < oldfile.txt > newfile.txt
```
***tip***
You can see contents of a file by using a command "cat"
Ex)
```sh
$ cat newfile.txt
```
#### pipeline '|'
Pipeline feeds output of previous command to input of next command.
Ex)
```sh
$ ls -lh | less
```
#### Expansion
special characters like "*" or "~" can be expansion.
Ex)
```sh
$ echo *
$ echo ~
```
#### Permission
Linux is a multi-user-system. So files and directories have a permission assinged differently to owner/group/others.
Permission is constructed by 9 numbers. 3/3/3 matchs each owner/group/others.
rwx: read and write and execute.
#### Superuser
A superuser has all system administation authority.
Put “sudo” before the command if you are a superuser.
#### Shell script
We can write and run shell script.