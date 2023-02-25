# <p align="center">SHELL - BASICS</p>

<img src="https://s3.eu-west-3.amazonaws.com/hbtn.intranet.project.files/holbertonschool-sysadmin_devops/205/image.jpg" width="100%"><br>

# <p align="center">RESSOURCE</p>
### Read or Watch: 

- [What Is "The Shell" ?](https://intranet.hbtn.io/rltoken/aygkrwOyI_yLtXHF1Yj0QQ)
- [Navigation](https://intranet.hbtn.io/rltoken/fMDkg3TKjANJSPTROMQSpA)
- [Looking Around](https://intranet.hbtn.io/rltoken/isPTWCOgTjeLaonZg8Rl5g)
- [A Guided Tour](https://intranet.hbtn.io/rltoken/GznRkhU3QTWAWwDeZ-k9Pw)
- [Manipuling Files](https://intranet.hbtn.io/rltoken/GA2UvOhDOjwa-NtbazvlCQ)
- [Working With Commands](https://intranet.hbtn.io/rltoken/ylGnKaanTSp3jIpXme9krg)
- [Reading Man Pages](https://intranet.hbtn.io/rltoken/52aXMywgSkXV07rFrX8eWw)
- [Keyboard Shortcuts For Bash](https://intranet.hbtn.io/rltoken/XXe2AD3TVWvNFwSP5_-YWQ)
- [LTS](https://wiki.ubuntu.com/LTS)
- [Shebang](https://intranet.hbtn.io/rltoken/_pJ5Fl2TaZVzW3jJy_mwKA)

--------------------

### Man or Help in Tzerminal
> cd | ls | pwd | less | file | ln | cp | mv | rm | mkdir | type | which | help | man  

There are many other useful Shell commands, but these basic commands are a good starting point for exploring and using the command-line interface.

--------------------

### Technologies
* [Emacs](https://www.gnu.org/software/emacs/)
* [Vim](https://doc.ubuntu-fr.org/vim/)
* script written in bash [Bash](https://datascientest.com/bash-tout-savoir/)
* Tested in Ubuntu [22.04 LTS](https://ubuntu.com/download/desktop/)

--------------------

### Requirements
- Allowed editors: `vi`, `vim`, `emacs`
- All your scripts will be tested on Ubuntu 20.04 LTS
- All your scripts should be exactly two lines long (`$ wc -l file` should print 2)
- All your files should end with a new line ([why?](http://unix.stackexchange.com/questions/18743/whats-the-point-in-adding-a-new-line-to-the-end-of-a-file/18789))
- The first line of all your files should be exactly `#!/bin/bash`
- A `README.md` file at the root of the repo, containing a description of the repository
- A `README.md` file, at the root of the folder of this project, describing what each script is doing
- You are not allowed to use backticks, `&&`, `||` or `;`
- All your scripts must be executable. To make your file executable, use the `chmod` command: `chmod u+x file`. Later, we’ll learn more about how to utilize this command.

--------------------

### More Info
Example of line count and first line
```c
julien@ubuntu:/tmp$ wc -l 12-file_type 
2 12-file_type
julien@ubuntu:/tmp$ head -n 1 12-file_type 
#!/bin/bash
julien@ubuntu:/tmp$ 
```

In order to test your scripts, you will need to use this command: `chmod u+x file`. We will see later what does `chmod` mean and do, but you can have a look at `man chmod` if you are curious.

Example
```c
julien@ubuntu:/tmp$ ls
12-file_type
lll
julien@ubuntu:/tmp$ ls -la lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ cat lll
#!/bin/bash
ls
julien@ubuntu:/tmp$ ls -l lll
-rw-rw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ chmod u+x lll # you do not have to understand this yet
julien@ubuntu:/tmp$ ls -l lll
-rwxrw-r-- 1 julien julien 15 Sep 19 21:05 lll
julien@ubuntu:/tmp$ ./lll
12-file_type
lll
julien@ubuntu:/tmp$ 
```  
<br><br>
# TASKS

### [0. Where Am I ?](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/0-current_working_directory)

>Write a script that prints the absolute path name of the current working directory.  

```c
$ ./0-current_working_directory
/0x00-shell_basics
$
```

--------------------

### [1. What's In There ?](https://github.com/Air-KS/holbertonschool-shell/blob/main/basics/1-listit)

>Display the contents list of your current directory.
```c
$ ./1-listit
Applications    Documents   Dropbox Movies Pictures
Desktop Downloads   Library Music Public
$
```

------------------------

### [2. There Is No Place Like Home](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/2-bring_me_home)

>Write a script that changes the working directory to the user’s home directory.

- You are not allowed to use any shell variables
```c
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ echo $HOME
/home/julien
julien@ubuntu:/tmp$ source ./2-bring_me_home
julien@ubuntu:~$ pwd
/home/julien
julien@ubuntu:~$ 
```

-------------------------

### [3. The Long Format](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/3-listfiles)

>Display current directory contents in a long format
```c
$ ./3-listfiles
total 32
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
$
```

-------------------------

### [4. Hidden Files](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/4-listmorefiles)

>Display current directory contents, including hidden files (starting with `.`). Use the long format.
```c
$ ./4-listmorefiles
total 32
drwxr-xr-x@ 6 sylvain staff 204 Jan 25 00:29 .
drwxr-xr-x@ 43 sylvain staff 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 sylvain staff 19 Jan 25 00:23 1-listit
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 sylvain staff 18 Jan 25 00:41 4-listmorefiles
$
```

--------------------------

### [5. I Love Numbers](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/5-listfilesdigitonly)

>Display current directory contents.
- Long format
- with user and group IDs displayed numerically
- And hidden files (starting with .)
```c++
$ ./5-listfilesdigitonly
total 32
drwxr-xr-x@ 6 501 20 204 Jan 25 00:29 .
drwxr-xr-x@ 43 501 20 1462 Jan 25 00:19 ..
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:19 0-current_working_directory
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:23 1-listfiles
-rwxr-xr-x@ 1 501 20 19 Jan 25 00:29 2-bring_me_home
-rwxr-xr-x@ 1 501 20 20 Jan 25 00:39 3-listfiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:41 4-listmorefiles
-rwxr-xr-x@ 1 501 20 18 Jan 25 00:43 5-listfilesdigitonly
$
```

-------------------------

### [6. Welcome](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/6-firstdirectory)

>Create a script that creates a directory named `my_first_directory` in the `/tmp/` directory.
```
$ ./6-firstdirectory
$ file /tmp/my_first_directory/
/tmp/my_first_directory/: directory
$
```

---------------------

### [7. Betty In My First Directory](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/7-movethatfile)

>Move the file `betty` from `/tmp/` to `/tmp/my_first_directory`.
```
$ ./7-movethatfile
$ ls /tmp/my_first_directory/
betty
$
```

-------------------------

### [8. Bye Bye Betty](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/8-firstdelete)

>Delete the file `betty`.
- he file `betty` is in `/tmp/my_first_directory`
```c
$ ./8-firstdelete
$ ls /tmp/my_first_directory/
$
```

-------------------------

### [9. Bye Bye My First Directory](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/9-firstdirdeletion)

>Delete the directory `my_first_directory` that is in the `/tmp` directory.
```c
$ ./9-firstdirdeletion
$ file /tmp/my_first_directory
/tmp/my_first_directory: cannot open `/tmp/my_first_directory' (No such file or directory)
$
```

-------------------------

### [10. Back To The Future](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/10-back)

>Write a script that changes the working directory to the previous one.
```c
julien@ubuntu:/tmp$ pwd
/tmp
julien@ubuntu:/tmp$ cd /var
julien@ubuntu:/var$ pwd
/var
julien@ubuntu:/var$ source ./10-back
/tmp
julien@ubuntu:/tmp$ pwd
/tmp
```

-----------------------------

### [11. Lists](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/11-lists)

>Write a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the `/boot` directory (in this order), in long format.

---------------------------

### [12. File Type](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/12-file_type)

>Write a script that prints the type of the file named `iamafile`. The file `iamafile` will be in the `/tmp` directory when we will run your script.
```c
ubuntu@ip-172-31-63-244:~$ ./12-file_type
/tmp/iamafile: ELF 64-bit LSB  executable, x86-64, version 1 (SYSV), dynamically linked (uses shared libs), for GNU/Linux 2.6.24, BuildID[sha1]=bd39c07194a778ccc066fc963ca152bdfaa3f971, stripped
```

-------------------------------

### [13. We Are Symbols, And Inhabit Symbols](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/13-symbolic_link)

>Create a symbolic link to `/bin/ls`, named `__ls__`. The symbolic link should be created in the current working directory.
```c
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
ubuntu@ip-172-31-63-244:/tmp/sym$./13-symbolic_link
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 144
drwxrwxr-x  2 ubuntu ubuntu   4096 Sep 20 03:24 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:24 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
```

-------------------------

### [14. Copy Html Files](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/14-copy_html)

>Create a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory.

You can consider that all HTML files have the extension `.html`

--------------------

### [15. Let's Move](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/15-lets_move)

>Create a script that moves all files beginning with an uppercase letter to the directory `/tmp/u`.  
>You can assume that the directory `/tmp/u` will exist when we will run your script
```c
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 My_file
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 Elif_ym
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
ubuntu@ip-172-31-63-244:/tmp/sym$ ./15-lets_move
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la
total 148
drwxrwxr-x  3 ubuntu ubuntu   4096 Sep 20 03:33 .
drwxrwxrwt 12 root   root   139264 Sep 20 03:26 ..
lrwxrwxrwx  1 ubuntu ubuntu      7 Sep 20 03:24 __ls__ -> /bin/ls
-rw-rw-r--  1 ubuntu ubuntu      0 Sep 20 03:32 random_file
ubuntu@ip-172-31-63-244:/tmp/sym$ ls -la /tmp/u
total 8
drwxrwxr-x 2 ubuntu ubuntu 4096 Sep 20 03:33 .
drwxrwxr-x 3 ubuntu ubuntu 4096 Sep 20 03:33 ..
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 My_file
-rw-rw-r-- 1 ubuntu ubuntu    0 Sep 20 03:32 Elif_ym
```

---------------------

### [16. Clean Emacs](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/16-clean_emacs)

Create a script that deletes all files in the current working directory that end with the character `~`.
```c
ubuntu@ip-172-31-63-244:/tmp/sym$ ls
main.c  main.c~  Makefile~
ubuntu@ip-172-31-63-244:/tmp/sym$ ./16-clean_emacs
ubuntu@ip-172-31-63-244:/tmp/emacs$ ls
main.c
ubuntu@ip-172-31-63-244:/tmp/emacs$
```

--------------------

### [17. Tree](https://github.com/Air-KS/holbertonschool-shell/blob/main/0x00-Shell_Basics/17-tree)

Create a script that creates the directories `welcome/`, `welcome/to/` and `welcome/to/school` in the current directory.

You are only allowed to use two spaces (and lines) in your script, not more.
```c
julien@ubuntu:/tmp/h$ ls -l
total 4
-rwxrw-r-- 1 julien julien 44 Sep 20 12:09 17-tree
julien@ubuntu:/tmp/h$ wc -l 17-tree 
2 17-tree
julien@ubuntu:/tmp/h$ head -1 17-tree 
#!/bin/bash
julien@ubuntu:/tmp/h$ tr -cd ' ' < 17-tree | wc -c # you do not have to understand this yet, but the result should be 2, 1 or 0
2
julien@ubuntu:/tmp/h$ ./17-tree 
julien@ubuntu:/tmp/h$ ls
17-tree  welcome
julien@ubuntu:/tmp/h$ ls welcome/
to
julien@ubuntu:/tmp/h$ ls -l welcome/to
total 4
drwxrwxr-x 2 julien julien 4096 Sep 20 12:11 school
julien@ubuntu:/tmp/h$ 
```

------------------------------

# Author
ROGERET Kevin<br>
> Project carried out within the framework of the school **[Holberton School](https://www.holbertonschool.com/).**<br>
