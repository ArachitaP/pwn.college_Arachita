# Shell Variables

## Printing Variables
Using echo command I printed the flag which was stored in the variable FLAG by using $ to access the variable.
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{8xpXCc_1eorul2misLu1ZVQxBTZ.QX3UTN0wCOykjNzEzW}
I learned how to print the content stored in a variable.

## Setting Variables
Assigned the value college to variable pwn using the assignment operator '='.
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{AZJsGi8Ioyx0NLC16wDPvEzf0y7.QX5UTN0wCOykjNzEzW}
I learned how to assign values to variables.

## Multi-word Variables
Used assignment operator '=' to assign the string as value to the variable and also used "" so that the string is considered as a whole.  
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{IrekBIQwGeHxltFT4zdapPmVgcT.QXwYTN0wCOykjNzEzW}
I leanred how to assign a string value to a variable

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

hacker@variables~printing-exported-variables:~$ export FLAG
hacker@variables~printing-exported-variables:~$ env $FLAG
env: ‘pwn.college{Q12DkQPLZhcC3cQRGIj82i6Speh.QX4UTN0wCOykjNzEzW}’: Permission denied
