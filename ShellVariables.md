# Shell Variables


## Printing Variables
The /challenge/run program will not, and cannot, give you the flag, but that's okay, because the flag has been put into the variable called "FLAG". Just have your shell print it out.
### Solve
Using echo command I printed the flag which was stored in the variable FLAG by using $ to access the variable.
```
**Flag:-** pwn.college{8xpXCc_1eorul2misLu1ZVQxBTZ.QX3UTN0wCOykjNzEzW}
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{8xpXCc_1eorul2misLu1ZVQxBTZ.QX3UTN0wCOykjNzEzW}
```
### New learning
I learned how to print the content stored in a variable.


## Setting Variables
To solve this level, you must set the PWN variable to the value COLLEGE. 
### Solve
Assigned the value college to variable pwn using the assignment operator '='.
**Flag:-** pwn.college{AZJsGi8Ioyx0NLC16wDPvEzf0y7.QX5UTN0wCOykjNzEzW}
```
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{AZJsGi8Ioyx0NLC16wDPvEzf0y7.QX5UTN0wCOykjNzEzW}
```
### New learning
I learned how to assign values to variables.


## Multi-word Variables
In this level, you'll need to set the variable PWN to COLLEGE YEAH. 
### Solve
Used assignment operator '=' to assign the string as value to the variable and also used "" so that the string is considered as a whole.
**Flag:-** pwn.college{IrekBIQwGeHxltFT4zdapPmVgcT.QXwYTN0wCOykjNzEzW}
```
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IrekBIQwGeHxltFT4zdapPmVgcT.QXwYTN0wCOykjNzEzW}
```
### New learning
I leanred how to assign a string value to a variable


## Exporting Variables
In this challenge, you must invoke /challenge/run with the PWN variable exported and set to the value COLLEGE, and the COLLEGE variable set to the value PWN but not exported 
### Solve
Used export command before inputting value into PWN variable and inputted value like normal into the COLLEGE varibale and ran the run program to get the flag.
**Flag:-** pwn.college{MbcIamNtnP4qITIXAVidHve-TNS.QXyYTN0wCOykjNzEzW}
```
hacker@variables~exporting-variables:~$ export PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run 
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great 
job! Here is your flag:
pwn.college{MbcIamNtnP4qITIXAVidHve-TNS.QXyYTN0wCOykjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```
### New learning
I leaned how to store export variales to other processes and child shells.

## Printing exported variables
There are multiple ways to access variables in bash. echo was just one of them, and we'll now learn at least one more in this challenge.
Try the env command: it'll print out every exported variable set in your shell, and you can look through that output to find the FLAG variable
### Solve
I first exported flag variable and then printed the exported file. 
**Flag:-** pwn.college{Q12DkQPLZhcC3cQRGIj82i6Speh.QX4UTN0wCOykjNzEzW}
```
hacker@variables~printing-exported-variables:~$ export FLAG
hacker@variables~printing-exported-variables:~$ env $FLAG
env: ‘pwn.college{Q12DkQPLZhcC3cQRGIj82i6Speh.QX4UTN0wCOykjNzEzW}’: Permission denied
```
### New learning
I leanred an another way to print flags provided it is exported to the shell.

## Storing command output
Read the output of the /challenge/run command directly into a variable called PWN, and it will contain the flag.
### Solve
Typed in the variable name and then assigned it value using '=' followed by the value in brakets, and the whole thing prepended by $, then the stored value in the variable is printed using echo command.
**Flag:-** pwn.college{QCKPKF90CkJXFiVRq64CFS9fNkI.QX1cDN1wCOykjNzEzW}
```
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run flag)
Congratulations! You have read the flag into the PWN variable. Now print it out 
and submit it!
hacker@variables~storing-command-output:~$ echo "$PWN"
pwn.college{QCKPKF90CkJXFiVRq64CFS9fNkI.QX1cDN1wCOykjNzEzW}
```
### New learning
I learned to store command outputs into a variable.


## Reading inputs
In this challenge, your job is to use read to set the PWN variable to the value COLLEGE.
### Solve
Used the read command with PWN as argument and then took input from the user whcih gave the flag.
**Flag:-** pwn.college{0IiAwxTYgruw3Umc4sdB0FUlJIS.QX4cTN0wCOykjNzEzW}
```
hacker@variables~reading-input:~$ read PWN
COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{0IiAwxTYgruw3Umc4sdB0FUlJIS.QX4cTN0wCOykjNzEzW}
```
### New learning
I learned how to sotre inputs from the user.


## Reading files
Read /challenge/read_me into the PWN environment variable, and get the flag.
### Solve
Used read command to read the content inside the variable and also used < to store the file value in the variable and then read it later.
**Flag:-** pwn.college{MhtgUIg27QE1O8FVOsLltgBtbwd.QXwIDO0wCOykjNzEzW}
```
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{MhtgUIg27QE1O8FVOsLltgBtbwd.QXwIDO0wCOykjNzEzW}
```
### New learning 
I learned how to store file values in variables and printing it without using cat.
