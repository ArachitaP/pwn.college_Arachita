# File Globbing
## Matching with *
The first glob we'll learn is *. When it encounters a * character in any argument, the shell will treat it as a "wildcard" and try to replace that argument with any files that match the pattern. 
Now, practice this yourself! Starting from your home directory, change your directory to /challenge, but use globbing to keep the argument you pass to cd to at most four characters! Once you're there, run /challenge/run for the flag!

We need to change the directory to challenge with just four words so we use find command to find the directory and then using cd command we change it to that directory.
### Solve
**Flag:-**
```
hacker@globbing~matching-with-:~$ cd /c*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8mRo46qrRpKdOjE3p29XmzGz9wA.QXxIDO0wCOykjNzEzW}
```

? symbol only finds that missing place letter by comparing the other lettters available. So just replace c and l with ?
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{0f3vdIpjvngEC-Fh3LC9aMpFn6j.QXyIDO0wCOykjNzEzW}

Change the directory using cd and the use [] to find the particular files required
```
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ file_[bash]
bash: file_a: command not found
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[bash]
You got it! Here is your flag!
pwn.college{MpkAOgSmx7tGpjJybxtC4hWXo6n.QXzIDO0wCOykjNzEzW}
```
I am accessing the file through home directory that is /home/hackers so while i need to specify the directory location while finding particular paths.
```
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[bash]
You got it! Here is your flag!
pwn.college{sITe9g7iZ5rvt6yCkCJ2vV6Dhjq.QX0IDO0wCOykjNzEzW}
```

```
hacker@globbing~multiple-globs:~$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run /*p*
Error: your argument is too long! It must be 3 characters or less.
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{cbbU18nn3tfOSa6UGBxPbJ7P14h.0lM3kjNxwCOykjNzEzW}
```
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

```
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files/
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{YHQ88KXCee74nne-QQRpDFarRAh.QX2IDO0wCOykjNzEzW}
```
