# File Globbing
## Matching with *
The first glob we'll learn is *. When it encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern. 
Now, practice this yourself! Starting from your home directory, change your directory to /challenge, but use globbing to keep the argument you pass to cd to at most four characters! Once you're there, run /challenge/run for the flag!
### Solve
Change the directory to challenge with just four words by find command to find the directory and then using cd command to change it to that directory.
**Flag:-** pwn.college{8mRo46qrRpKdOjE3p29XmzGz9wA.QXxIDO0wCOykjNzEzW}
```
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8mRo46qrRpKdOjE3p29XmzGz9wA.QXxIDO0wCOykjNzEzW}
```
### New Learning
I learned to use * command to find directories.

## Matching with ?
Next, let's learn about ?. When it encounters a ? character in any argument, the shell will treat it as a single-character wildcard. This works like *, but only matches one character. 
Now, practice this yourself! Starting from your home directory, change your directory to /challenge, but use the ? character instead of c and l in the argument to cd! Once you're there, run /challenge/run for the flag!
### Solve
Use ? symbol to replace c and l in challenge directory and then get the flag. 
**Flag:-** pwn.college{0f3vdIpjvngEC-Fh3LC9aMpFn6j.QXyIDO0wCOykjNzEzW}
```
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0f3vdIpjvngEC-Fh3LC9aMpFn6j.QXyIDO0wCOykjNzEzW}
```
### New learning
I learned to use ? command. It finds that missing place letter by comparing the other lettters available.

## Matching with []
The square brackets are, essentially, a limited form of ?, in that instead of matching any character, [] is a wildcard for some subset of potential characters, specified within the brackets. For example, [pwn] will match the character p, w, or n.
Change your working directory to /challenge/files and run /challenge/run with a single argument that bracket-globs into file_b, file_a, file_s, and file_h
### Solve
Change the directory using cd and the use [] to find the particular files required.
**Flag:-** pwn.college{MpkAOgSmx7tGpjJybxtC4hWXo6n.QXzIDO0wCOykjNzEzW}
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ file_[bash]
bash: file_a: command not found
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{MpkAOgSmx7tGpjJybxtC4hWXo6n.QXzIDO0wCOykjNzEzW}
```
### New learning
I learned to use [] command to fina a set of files with of similar characters.

## Matching paths with []
Globbing happens on a path basis, so you can expand entire paths with your globbed arguments.
Once more, we've placed a bunch of files in /challenge/files. Starting from your home directory, run /challenge/run with a single argument that bracket-globs into the absolute paths to the file_b, file_a, file_s, and file_h files!
### Solve
Access the file through home directory that is /home/hackers by specifying the directory location while finding particular paths.
**Flag:-** pwn.college{sITe9g7iZ5rvt6yCkCJ2vV6Dhjq.QX0IDO0wCOykjNzEzW}
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{sITe9g7iZ5rvt6yCkCJ2vV6Dhjq.QX0IDO0wCOykjNzEzW}
```
### New learning
I learned how to access the file through home directory by specifying the path and then finding the required files using [].

## Multiple globs
 We put a few happy, but diversely-named files in /challenge/files. Go cd there and run /challenge/run, providing a single argument: a short (3 characters or less) globbed word with two * globs in it that covers every word that contains the letter p.
### Solve
Went to the challenge files directory and then did challenge run and passed *p* as an argument.
**Flag:-** pwn.college{cbbU18nn3tfOSa6UGBxPbJ7P14h.0lM3kjNxwCOykjNzEzW}
```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run /*p*
Error: your argument is too long! It must be 3 characters or less.
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{cbbU18nn3tfOSa6UGBxPbJ7P14h.0lM3kjNxwCOykjNzEzW}
```
### New learning
I learned how multiple globbing works. * fills the letters before the specified word and * fills the letters after the specified word.

## Mixing globs
Now, let's put the previous levels together! We put a few happy, but diversely-named files in /challenge/files. Go cd there and, using the globbing you've learned, write a single, short (6 characters or less) glob that (when passed as an argument to /challenge/run) will match the files "challenging", "educational", and "pwning"
### Solve
Changed directory to challenge files and then ran the file using [cep]* as argument as c,e,p are unique starting points for the files and * autocompletes the names of the files
**Flag:-** pwn.college{oQUGnskt9byMj2_Mp_8zdN4841l.QX1IDO0wCOykjNzEzW}
```
hacker@globbing~mixing-globs:~$ cd /challenge/files/
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]
Your expansion did not expand to the requested files (challenging, educational, 
pwning). Instead, it expanded to:
[cep]
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{oQUGnskt9byMj2_Mp_8zdN4841l.QX1IDO0wCOykjNzEzW}
```
### New learning
I learned how to mix globs for better use and efficiency.

## Exclusionary globbing
Go forth to /challenge/files and run /challenge/run with all files that don't start with p, w, or n.
### Solve
Got into the directory and did /challenge/run to run the file with [^pwn]* as an argument because ^ will exclude all file starting with p,w,n.
**Flag:-** pwn.college{YHQ88KXCee74nne-QQRpDFarRAh.QX2IDO0wCOykjNzEzW}
```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{YHQ88KXCee74nne-QQRpDFarRAh.QX2IDO0wCOykjNzEzW}
```
### New learning
I learned how to exclude the files I don't want.

## Tab completion
This challenge has copied the flag into /challenge/pwncollege, and you can freely cat that file. But you can't type the filename: we used some serious trickery to make sure that you must tab-complete it.
### Solve
Used cat command and then tab key for completion and faster work.
**Flag:-** pwn.college{UWvbwVA1tXg8f0nIZQ-CNAjWrE9.0FN0EzNxwCOykjNzEzW}
```
hacker@globbing~tab-completion:~$ ls /challenge
DESCRIPTION.md  pwncollege​
hacker@globbing~tab-completion:~$ /challenge/p
bash: /challenge/p: No such file or directory
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege​ 
pwn.college{UWvbwVA1tXg8f0nIZQ-CNAjWrE9.0FN0EzNxwCOykjNzEzW}
```
### New learning
Using tab key to autofill.

## Multiple options for tab completion
This challenge has a /challenge/files directory with a bunch of files starting with pwncollege. Tab-complete from /challenge/files/p or so, and make your way to the flag
### Solve
Used  cat command and then to autofill the directory
**Flag:-** pwn.college{o3rQPm2hiVdV2uf483Dji60Hrf6.0lN0EzNxwCOykjNzEzW}
```
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{o3rQPm2hiVdV2uf483Dji60Hrf6.0lN0EzNxwCOykjNzEzW}
```
### New learning
I learned more broader usage of tab key.

## Tab completion on commands
Tab completion is for more than files! You can also tab-complete commands. This level has a command that starts with pwncollege, and it'll give you the flag.
### Solve
Type pwncollege and tab to autofill the command and press enter to get the flag.
**Flag:-** pwn.college{UwPebEIuAL-zZvfTebj9Q_jN4Tq.0VN0EzNxwCOykjNzEzW}
```
hacker@globbing~tab-completion-on-commands:~$ pwncollege-13065 
Correct! Here is your flag:
pwn.college{UwPebEIuAL-zZvfTebj9Q_jN4Tq.0VN0EzNxwCOykjNzEzW}
```
### New learning
I learned how tab can be used to complete commands.
