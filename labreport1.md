# Lab Report 1

## "cd" Command

**1. Share an example of using the command with no arguments.**
```
[user@sahara ~]$ cd cse15l-lab-reports
[user@sahara ~/cse15l-lab-reports]$ pwd
/home/cse15l-lab-reports
[user@sahara ~/cse15l-lab-reports]$ cd
[user@sahara ~]$ pwd
/home
[user@sahara ~]$ 
```
This command changes the directory. The current working directory is cse15l-lab-reports. When the command is used without an argument and the working directory is printed, it changes the working directory back to /home because no path is specified to change into.
<br>
The output is not an error.

**2. Share an example of using the command with a path to a *directory* as an argument.**
```
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ pwd
/home/lecture1/messages
```
This command successfully changes the current directory, lecture1. When the directory, messages, is used as a path with the command, the working directory changes to /home/lecture1/messages.
<br>
The output is not an error.

**3. Share an example of using the command with a path to a *file* as an argument**
```
[user@sahara ~/cse15l-lab-reports]$ cd clouds.md
bash: cd: clouds.md: Not a directory
```
The current working directory is cse15l-lab-reports. There is no output because a relative path to a file does not work with this command since it is not a working directory. Files are stored in directories, so the command is unable to change the directory to the file clouds.md.
<br>
The output is an error because clouds.md is not a directory since it is a file and not a folder.

---

## "ls" Command

**1. Share an example of using the command with no arguments.**
```
[user@sahara ~/cse15l-lab-reports]$ ls
clouds.md  index.md  labreport1.md
```
This command lists the files and folders in the output. The current working directory is cse15l-lab-reports. Based on the output without arguments, it lists the files and folders within the current working directory. In this case, the three files in the working directory are listed out which are clouds.md, index.md, and labreport1.md.
<br>
The output is not an error.

**2. Share an example of using the command with a path to a *directory* as an argument.**
```
[user@sahara ~/lecture1]$ ls messages
en-us.txt  es-mx.txt  ja.txt  zh-cn.txt
```
This command with a directory as its path lists out the files within the folder. The current working directory is lecture1, and when the command is used with messages as its path, it gives an output of the 4 files within the messages folder. This consists of en-us.txt, es-mx.txt, ja.txt, and zh-cn.txt.
<br>
The output is not an error.

**3. Share an example of using the command with a path to a *file* as an argument.**
```
[user@sahara ~/cse15l-lab-reports]$ ls clouds.md
clouds.md
```
This command lists out files and folders within the given path. The current working directory is cse15l-lab-reports. Since there are no other files within the clouds.md file, it just returns that file itself in the output. Since files cannot be contained within other files, no other files would be listed, so it would have to be within a folder in order to be listed.
<br>
The output is not an error.

---

## "cat" Command

**1. Share an example of using the command with no arguments.**
```
[user@sahara ~/cse15l-lab-reports]$ cat
hello
hello
world 
world
^C
[user@sahara ~/cse15l-lab-reports]$ 
```
This command prints out the contents of the path that is given. The current working directory is cse15l-lab-reports. Since there was no file in the path given, it returns whatever is written in the terminal input.
<br>
The output is not an error.

**2. Share an example of using the command with a path to a *directory* as an argument.**
```
[user@sahara ~/lecture1]$ cat messages
cat: messages: Is a directory
```
The current working directory is lecture1. This command prints out the contents of a file, not a directory folder, so it does not end up printing out anything.
<br>
The output is an error because cse15l-lab-reports is a folder and not a file.

**3. Share an example of using the command with a path to a *file* as an argument.**
```
[user@sahara ~/cse15l-lab-reports]$ cat clouds.md
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
This command prints out the contents of a file. The current working directory is cse15l-lab-reports and when cat is used on a file within this directory folder, it successfully prints out the contents of clouds.md because that file is given as a path.
<br>
The output is not an error.
