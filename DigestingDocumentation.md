# Digesting Documentation
## Learning From Documentation
The program for this challenge is /challenge/challenge, and you'll need to invoke it properly in order for it to give you the flag. To properly run this program, you will need to pass it the argument of --giveflag. 
### Solve
Passed the --give flag argument to the specified directory to get the flag.

**Flag:-** pwn.college{0D4mMcod8JdRa_QFHRocinCWr1y.QX0ITO0wCOykjNzEzW}
```
hacker@man~learning-from-documentation:~$ /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{0D4mMcod8JdRa_QFHRocinCWr1y.QX0ITO0wCOykjNzEzW}
```
### New Learning
I learned to read documentations.

## Learning complex usuage
This program allows you to print arbitrary files to the terminal, when given the --printfile argument. The argument to the --printfile argument is the path of the flag to read. For example, /challenge/challenge --printfile /challenge/DESCRIPTION.md will print out the description of the level!
### Solve
Read the documentation and passed the specified argument to read the file.

**Flag:-** pwn.college{IlEwlsQJ4c1WD42fn2_QWJcEYM_.QX1ITO0wCOykjNzEzW}
```
hacker@man~learning-complex-usage:~$ /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{IlEwlsQJ4c1WD42fn2_QWJcEYM_.QX1ITO0wCOykjNzEzW}
```
### New Learning
I learned to read documentations and different arguments being passed.

## Reading manuals
The challenge in this level has a secret option that, when you use it, will cause the challenge to print the flag. You must learn this option through the man page for challenge
### Solve
Used the man command to read the manual challenge. Then passed the given commands in the output of the manual as arguments out of which jbbamy 489 had the flag.

**Flag:-** pwn.college{4DjGTbE8bamGRyQzeOm9USQhJNl.QX0EDO0wCOykjNzEzW}
```
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --fortune 
Sure he's sharp as a razor ... he's a two-dimensional pinhead!
hacker@man~reading-manuals:~$ /challenge/challenge  --version
I'm exactly the version I need to be!
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --jbbamy NUM
Incorrect usage! Please read the challenge man page!
hacker@man~reading-manuals:~$ man challenge
hacker@man~reading-manuals:~$ /challenge/challenge  --jbbamy 489
Correct usage! Your flag: pwn.college{4DjGTbE8bamGRyQzeOm9USQhJNl.QX0EDO0wCOykjNzEzW}
```
### New Learning
I learned to read documentations and different arguments being passed.

## Searching manuals
You can scroll man pages with the arrow keys (and PgUp/PgDn) and search with /. After searching, you can hit n to go to the next result and N to go to the previous result. Instead of /, you can use ? to search backwards!
Find the option that will give you the flag by reading the challenge man page.
### Solve
First I opened the manual challenge, then i searched for flag using '/flag' attribute whoch showed me the designated line where it is, then using that argument I found the flag.

**Flag:-** pwn.college{QgtV_Z_mk4argYMGEgrq1l1CNoO.QX1EDO0wCOykjNzEzW}
```
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --oe
Initializing...
Correct usage! Your flag: pwn.college{QgtV_Z_mk4argYMGEgrq1l1CNoO.QX1EDO0wCOykjNzEzW}
```
### New Learning
I learned about different commands to find the man pages.

