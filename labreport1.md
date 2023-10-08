# Lab Report 1

## "cd" Command

**1. Share an example of using the command with no arguments.**
```
[user@sahara ~]$ cd
[user@sahara ~]$ 
```
This command changes the directory. Since there are no arguments, there is no path to change the directory, which explains why there is no output. 
<br>
The output is not an error.

**2. Share an example of using the command with a path to a *directory* as an argument.**
```
[user@sahara ~]$ cd cse15l-lab-reports/
[user@sahara ~/cse15l-lab-reports]$
```
This command successfully changes the current directory to cse15l-lab-reports because of the path it receives.
The output is not an error.

**3. Share an example of using the command with a path to a *file* as an argument**
```
[user@sahara ~]$ cd cse15l-lab-reports/clouds.md
bash: cd: cse15l-lab-reports/clouds.md: Not a directory
```
There is no output because a relative path to a file does not work with this command since it is not a working directory. Files are stored in directories, so the command is unable to change the directory to the file clouds.md.
The output is an error because clouds.md is not a directory since it is a file and not a folder.

---

## "ls" Command

**1. Share an example of using the command with no arguments.**
```
[user@sahara ~]$ ls
cse15l-lab-reports  lecture1
```
This command lists the files and folders in the output. Based on the output without arguments, it lists the two folders cse15l-lab-reports and lecture1.
The output is not an error.

**2. Share an example of using the command with a path to a *directory* as an argument.**
```
[user@sahara ~]$ ls cse15l-lab-reports/
clouds.md  index.md  labreport1.md
```
This command with a directory as its path lists out the three files within the folder cse15l-lab-reports.
The output is not an error.

**3. Share an example of using the command with a path to a *file* as an argument.**
```
[user@sahara ~]$ ls cse15l-lab-reports/clouds.md
cse15l-lab-reports/clouds.md
```
This command lists out files and folders within the given path. Since there are no other files within the clouds.md file, it just returns that file itself in the output.
The output is not an error.

---

## "cat" Command

**1. Share an example of using the command with no arguments.**
```
[user@sahara ~]$ cat
hello
hello
world
world
^C
[user@sahara ~]$
```
This command prints out the contents of the path that is given. Since there was no file in the path given, it returns whatever is written in the terminal input.
The output is an error because it prints out the input until control+c terminates the command.

**2. Share an example of using the command with a path to a *directory* as an argument.**
```
[user@sahara ~]$ cat cse15l-lab-reports/
cat: cse15l-lab-reports/: Is a directory
```
This command prints out the contents of a file, not a directory folder, so it does not end up printing out anything.
The output is an error because cse15l-lab-reports is a folder and not a file.

**3. Share an example of using the command with a path to a *file* as an argument.**
```
[user@sahara ~]$ cat cse15l-lab-reports/clouds.md
*Welcome*
**Lab Report 1**
## In the clouds!
[Cheatsheet Link](https://commonmark.org/help/)
![Image](https://images.pexels.com/photos/19670/pexels-photo.jpg?cs=srgb&dl=pexels-miguel-%C3%A1-padri%C3%B1%C3%A1n-19670.jpg&fm=jpg)
> Not coming down for a while
# Grocery List
- apples
- bananas
- strawberries
---
# To Do List
1. wake up
2. walk the dog
3. eat breakfast
```
This command prints out the contents of a file, which successfully does so displaying the contents of the clouds.md file.
The output is not an error.







