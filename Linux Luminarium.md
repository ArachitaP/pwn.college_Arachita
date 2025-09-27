# Pondering Paths
## The Root
Alright, so the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag. All you need to do for this level is to invoke this program!

You can invoke a program by providing its path on the command line. In this case, you'll be giving the exact path, starting from /, so the path would be /pwn. This style of path, one that starts with the root directory, is referred to as an "absolute path".

Start the challenge, launch a terminal, invoke the pwn program using its absolute path, and Capture that Flag! Good luck!
### Solve
**Flag:-** pwn.college{8ApQUF3_WiWlK3P_cQKVfQNGMGK.QX4cTO0wCOykjNzEzW}
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{8ApQUF3_WiWlK3P_cQKVfQNGMGK.QX4cTO0wCOykjNzEzW}
```
### New Learning
I learned how to access programs from a file system.

## Program and absolute paths
Let's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/). The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.

This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the run file that is in the challenge directory that is, in turn, in the / directory. If you invoke the challenge correctly, it will give you the flag. Good luck!
### Solve
**Flag:-** pwn.college{gQ0ZXYFXIdaJ6GkNWCyxUJ9xx6j.QX1QTN0wCOykjNzEzW}
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{gQ0ZXYFXIdaJ6GkNWCyxUJ9xx6j.QX1QTN0wCOykjNzEzW}
```
### New Learning
I learned how to access program which is there inside the directory in a root directory.

## Position thy self
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:

hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!
### Solve
**Flag:-** pwn.college{0qOJlV-LDDRd3FCrN4B8hCjy4XI.QX2QTN0wCOykjNzEzW}
```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /var/lib/apt/lists directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /var/lib/apt/lists
hacker@paths~position-thy-self:/var/lib/apt/lists$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{0qOJlV-LDDRd3FCrN4B8hCjy4XI.QX2QTN0wCOykjNzEzW}
```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/bin directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/bin
hacker@paths~position-elsewhere:/usr/bin$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{sS_AYdstGoo5cQvaL_36hV_4Y9Z.QX3QTN0wCOykjNzEzW}
```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /etc/apt/sources.list.d directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /etc/apt/sources.list.d/
hacker@paths~position-yet-elsewhere:/etc/apt/sources.list.d$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{4by6pzBxzdM3AQRgcfwDWi8n7XH.QX4QTN0wCOykjNzEzW}
```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{ohk1JndFNfvQBdMOiJSrZJk5JFR.QX5QTN0wCOykjNzEzW}
```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run 
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{wK0sT556C5wp5hBZFc4BzkJ2zbt.QXwUTN0wCOykjNzEzW}
```
hacker@paths~implicit-relative-path:~$ cd /challenge/
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{QfHVMD-x2JTBIFCThJyohLpAnqr.QXxUTN0wCOykjNzEzW}
```
hacker@paths~home-sweet-home:~$ /challenge/run
You must provide an argument to /challenge/run when you invoke it!
hacker@paths~home-sweet-home:~$ /challenge/run ~/a
Writing the file to /home/hacker/a!
... and reading it back to you:
pwn.college{osXNgW_JeKL9NFNev0J2w92EoCa.QXzMDO0wCOykjNzEzW}
```
