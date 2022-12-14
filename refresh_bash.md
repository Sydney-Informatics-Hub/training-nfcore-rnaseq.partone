---
title: "Refresh your unix shell (bash) skills"
teaching: 0
exercises: 15
questions:
- "What is a terminal window?"
- "How are your basic bash skills?"
objectives:
- "Refresh your bash skills"
- "Run some basic bash commands"
keypoints:
- "The two important commands we used were 'pwd' and 'cd'"

---




### Navigate in a bash terminal

Let’s first navigate to our instance’s home (you could omit ~ to get home, too):

```
$ cd ~
```

Check the path of the current working directory:

```
$ pwd
```

```
/home/training
```

Go to the parent directory of the current one:
```
$ cd ..
```

Check where you are:
```
$ pwd
```
```
/home
```

### Handling directories and files

Make a directory called `temp`

```
mkdir temp
```

Check if the the new directory is present
```
ls -lh
```
```
drwxrwxr-x 2 training training 4.0K Sep  1 09:16 temp
```

Now navigate into to the `temp` directory :
```
$ cd temp/
```

To make a new file, e.g. an empty text file:
```
$ touch empty.txt
```
We can check the content of this directory, to see whether the file has been created:
```
$ ls
```
```
empty.txt
```

Get details about files and directories with:
```
$ ls -lh 
```
```
-rw-rw-r-- 1 training training 0 Sep  1 09:18 empty.txt
```

To make a copy of a file with another name:
```
$ cp empty.txt empty-copy.txt 
```
To rename a file:
```
$ mv empty-copy.txt empty-second.txt
```

To move a file to another directory, e.g. your home (still mv, but now the second argument is an existing directory):
```
$ mv empty-second.txt /home/training/
```

Now let’s remove both files:
```
$ rm empty.txt /home/training/empty-second.txt
```

### Visualising contents of text files.

Let’s create a text file with some words in it. We’ll use a popular, friendly text editor called nano:
```
$ nano words.txt
```
- In the editor screen, write something random.
- To save this text, press Ctrl-O, then Enter.
- To exit, press Ctrl-X.

- Now we want to visualise the contents of this file on our terminal.
- We can use cat to display it all in one go:
```
$ cat words.txt
```
```
- random words that we just saved in this file
```

For very long files, we might want to be able to navigate the content in chunks. We can achieve this with less:
```
$ less words.txt
```
- Go forward by pressing Ctrl-F, go backwards with Ctrl-B.
- Quit the navigation by pressing q.


{% include links.md %}
