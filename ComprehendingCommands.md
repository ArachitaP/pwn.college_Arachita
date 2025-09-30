# Comprehending commands

## cat: not the pet, but the command
One of the most critical Linux commands is cat. cat is most often used for reading out files, like so:
cat will concatenate (hence the name) multiple files if provided multiple arguments.
Finally, if you give no arguments at all, cat will read from the terminal input and output it.

In this challenge, I will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!
### Solve
Did cat flag to read out the flag.
**Flag:-** pwn.college{EhJyLEJqXQ9Pe2pzoYFQp2zjAXr.QXxcTN0wCOykjNzEzW}
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{EhJyLEJqXQ9Pe2pzoYFQp2zjAXr.QXxcTN0wCOykjNzEzW}
```
### New Learning
I learned how to use the cat command.


## Catting absolute paths
In the last level, you did cat flag to read the flag out of your home directory! You can, of course, specify cat's arguments as absolute paths:

In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.
FUN FACT: /flag is where the flag always lives in pwn.college, but unlike in this challenge, you typically can't access that file directly.
### Solve
Used cat command and /flag as an argument to get the flag
**Flag:-** pwn.college{gzn-6EtM4y3fvJpj6ALbVM_knXy.QX5ETO0wCOykjNzEzW}
```
hacker@commands~catting-absolute-paths:~$ cat/flag
bash: cat/flag: No such file or directory
hacker@commands~catting-absolute-paths:~$ cat/challenge/flag
bash: cat/challenge/flag: No such file or directory
hacker@commands~catting-absolute-paths:~$ cd /
hacker@commands~catting-absolute-paths:/$ cat flag
pwn.college{gzn-6EtM4y3fvJpj6ALbVM_knXy.QX5ETO0wCOykjNzEzW}
```
### New Learning
I learned how to cat absolute paths.


## More catting practice
You can specify all sorts of paths as arguments to commands, and we'll practice some more with cat. In this level, I'll put the flag in some crazy directory, and I will not allow you to change directories with cd, so no cat flag for you. You must retrieve the flag by absolute path, wherever it is
### Solve
Used cat command and specified the directory as an argument to get the flag.
**Flag:-**
```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/share/applications/flag. Go cat it out **without** cding into 
that directory!
hacker@commands~more-catting-practice:~$ cat /usr/share/applications/flag
pwn.college{gfdNlCPHmT-m_XZHiK2owihGYK9.QXwITO0wCOykjNzEzW}
```
### New Learning
I learned how to use cat more properly.


## Greeping for a needle in haystack
In this challenge, I've put a hundred thousand lines of text into the /challenge/data.txt file. grep it for the flag.
### Solve
Used grep command int the specified directory to get the specific line where the flag is.
**Flag:-** pwn.college{YZigmbXmuPxGLF2RF8GnT2ppa5q.QX3EDO0wCOykjNzEzW}
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{YZigmbXmuPxGLF2RF8GnT2ppa5q.QX3EDO0wCOykjNzEzW}
```
### New Learning
I learned how to search specific contents in a file.


## Comparing files
Now for your challenge! There are two files in /challenge:

/challenge/decoys_only.txt contains 100 fake flags
/challenge/decoys_and_real.txt contains all 100 fake flags plus the one real flag

Use diff to find what's different between these files and get your flag
### Solve
Used diff command to find the difference between the two lines that is the flag line in one of them, to get the flag.
**Flag:-** pwn.college{kc5DrePIejuBZzmex54g_2eggY8.01MwMDOxwCOykjNzEzW}
```
hacker@commands~comparing-files:~$ cat /challenge/decoys_only.txt
pwn.college{fake_flag_number_1_sKOcWfwvtpM}
pwn.college{fake_flag_number_2_P68bLeZmrPQ}
pwn.college{fake_flag_number_3_YHfsdpr9YVM}
pwn.college{fake_flag_number_4_Ysbn87N69zk}
pwn.college{fake_flag_number_5_w02MH2iFDa8}
pwn.college{fake_flag_number_6_Nng4rqT6Wo}
pwn.college{fake_flag_number_7_XvqEWgXnT2k}
pwn.college{fake_flag_number_8_6RI0hGWgHkI}
pwn.college{fake_flag_number_9_TEJ4l6kNlqU}
pwn.college{fake_flag_number_10_sS4CEvVdR14}
pwn.college{fake_flag_number_11_oXhC2i9LYCc}
pwn.college{fake_flag_number_12_HdHaaNbYHfU}
pwn.college{fake_flag_number_13_9gLG6XGaQXw}
pwn.college{fake_flag_number_14_1DjDy8FTfs}
pwn.college{fake_flag_number_15_imS8NbhDm10}
pwn.college{fake_flag_number_16_kWtFnvrxMYE}
pwn.college{fake_flag_number_17_kWfHxEz40UE}
pwn.college{fake_flag_number_18_u9KbstYtEtM}
pwn.college{fake_flag_number_19_NGPhhUrmms}
pwn.college{fake_flag_number_20_qyZll55AVrY}
pwn.college{fake_flag_number_21_HCJVol6l8IU}
pwn.college{fake_flag_number_22_0iXfSaLRLpM}
pwn.college{fake_flag_number_23_ULTSK3bieL8}
pwn.college{fake_flag_number_24_TcOJBi3mgXE}
pwn.college{fake_flag_number_25_hkUZL20Cg}
pwn.college{fake_flag_number_26_gZKwZeFARuQ}
pwn.college{fake_flag_number_27_w9Lv2ZTEU}
pwn.college{fake_flag_number_28_rhiQyYPKUk}
pwn.college{fake_flag_number_29_Tl3xIC92RYc}
pwn.college{fake_flag_number_30_EgCuo6hTYQA}
pwn.college{fake_flag_number_31_SMdRfjm7c}
pwn.college{fake_flag_number_32_NEvMHHCMPpY}
pwn.college{fake_flag_number_33_Y5Nu5sFGYTo}
pwn.college{fake_flag_number_34_xp9xsBAM90}
pwn.college{fake_flag_number_35_mdYl32SLbM}
pwn.college{fake_flag_number_36_JF25mvQQyE}
pwn.college{fake_flag_number_37_XECS3zP7laA}
pwn.college{fake_flag_number_38_ONXeId9SJo}
pwn.college{fake_flag_number_39_GsYKtMPL4iE}
pwn.college{fake_flag_number_40_ZPmJHEMXdlU}
pwn.college{fake_flag_number_41_AteXJKpWUho}
pwn.college{fake_flag_number_42_6uPmolfaYqk}
pwn.college{fake_flag_number_43_nfMaQeeV9w}
pwn.college{fake_flag_number_44_CMf0aHvuUE}
pwn.college{fake_flag_number_45_Ywgh7SVg1nE}
pwn.college{fake_flag_number_46_uSZqHmbhg7E}
pwn.college{fake_flag_number_47_xDNMkwWm5w}
pwn.college{fake_flag_number_48_cq7TQPI58qc}
pwn.college{fake_flag_number_49_1zb8V2tCXEM}
pwn.college{fake_flag_number_50_82JpSC0PbrI}
pwn.college{fake_flag_number_51_ZkhYgR9xEJk}
pwn.college{fake_flag_number_52_Y8IU8FZvyoA}
pwn.college{fake_flag_number_53_1rJdWQvGcoo}
pwn.college{fake_flag_number_54_KGS3zV2ySO4}
pwn.college{fake_flag_number_55_LXkF3yppdZQ}
pwn.college{fake_flag_number_56_rjbqJWiIWw}
pwn.college{fake_flag_number_57_qqebUGK8xo0}
pwn.college{fake_flag_number_58_RVD8N64laMU}
pwn.college{fake_flag_number_59_VfpGQaD4KA}
pwn.college{fake_flag_number_60_OQxXfFzdkSM}
pwn.college{fake_flag_number_61_C6n4QWw30Yk}
pwn.college{fake_flag_number_62_ktKxrOb511A}
pwn.college{fake_flag_number_63_Cx7T5QSVTc}
pwn.college{fake_flag_number_64_dhgnPhACo}
pwn.college{fake_flag_number_65_tHe3UMRMDo}
pwn.college{fake_flag_number_66_TNGHfHvxZw}
pwn.college{fake_flag_number_67_7v0vIHDdDBU}
pwn.college{fake_flag_number_68_9OY0ODfUC5w}
pwn.college{fake_flag_number_69_BRXbMpTpoE}
pwn.college{fake_flag_number_70_sJ2mJbikTzc}
pwn.college{fake_flag_number_71_lfYgdkjW3U}
pwn.college{fake_flag_number_72_9uPTDDgmIhw}
pwn.college{fake_flag_number_73_B9O6bAMOVGs}
pwn.college{fake_flag_number_74_xI4oDaqB9W4}
pwn.college{fake_flag_number_75_PiPFbyebH8}
pwn.college{fake_flag_number_76_T4uHTMUiS8}
pwn.college{fake_flag_number_77_kA0ap0MZA}
pwn.college{fake_flag_number_78_MBej7L9Rkbk}
pwn.college{fake_flag_number_79_zfLinYLB67M}
pwn.college{fake_flag_number_80_TKzh8YQxIk}
pwn.college{fake_flag_number_81_vuiywaZcQ}
pwn.college{fake_flag_number_82_uoPMyVt59eY}
pwn.college{fake_flag_number_83_hM1hFzOzHY}
pwn.college{fake_flag_number_84_xSHKcIIeC1Y}
pwn.college{fake_flag_number_85_QUn40k9r88}
pwn.college{fake_flag_number_86_ziPMRBkQbw}
pwn.college{fake_flag_number_87_H5YvZ66uoo0}
pwn.college{fake_flag_number_88_ZlnscXGMGI}
pwn.college{fake_flag_number_89_Q8gNq8DfyA}
pwn.college{fake_flag_number_90_ZO881jGMjds}
pwn.college{fake_flag_number_91_ddpDX99yk3g}
pwn.college{fake_flag_number_92_ouSot9dPndo}
pwn.college{fake_flag_number_93_KE8OjWFQL0}
pwn.college{fake_flag_number_94_wjEyA7tFS0M}
pwn.college{fake_flag_number_95_VQ2pqG3arU}
pwn.college{fake_flag_number_96_1eUax8g7xdg}
pwn.college{fake_flag_number_97_JRzNJgSguY}
pwn.college{fake_flag_number_98_9cFkSdCpSI}
pwn.college{fake_flag_number_99_YgenUlPy6ok}
pwn.college{fake_flag_number_100_nO5ExlHfJag}
hacker@commands~comparing-files:~$ cat /challenge/decoys_and_real.txt
pwn.college{fake_flag_number_1_sKOcWfwvtpM}
pwn.college{fake_flag_number_2_P68bLeZmrPQ}
pwn.college{fake_flag_number_3_YHfsdpr9YVM}
pwn.college{fake_flag_number_4_Ysbn87N69zk}
pwn.college{fake_flag_number_5_w02MH2iFDa8}
pwn.college{fake_flag_number_6_Nng4rqT6Wo}
pwn.college{fake_flag_number_7_XvqEWgXnT2k}
pwn.college{fake_flag_number_8_6RI0hGWgHkI}
pwn.college{fake_flag_number_9_TEJ4l6kNlqU}
pwn.college{fake_flag_number_10_sS4CEvVdR14}
pwn.college{fake_flag_number_11_oXhC2i9LYCc}
pwn.college{fake_flag_number_12_HdHaaNbYHfU}
pwn.college{fake_flag_number_13_9gLG6XGaQXw}
pwn.college{fake_flag_number_14_1DjDy8FTfs}
pwn.college{fake_flag_number_15_imS8NbhDm10}
pwn.college{fake_flag_number_16_kWtFnvrxMYE}
pwn.college{fake_flag_number_17_kWfHxEz40UE}
pwn.college{fake_flag_number_18_u9KbstYtEtM}
pwn.college{fake_flag_number_19_NGPhhUrmms}
pwn.college{fake_flag_number_20_qyZll55AVrY}
pwn.college{fake_flag_number_21_HCJVol6l8IU}
pwn.college{fake_flag_number_22_0iXfSaLRLpM}
pwn.college{fake_flag_number_23_ULTSK3bieL8}
pwn.college{fake_flag_number_24_TcOJBi3mgXE}
pwn.college{fake_flag_number_25_hkUZL20Cg}
pwn.college{fake_flag_number_26_gZKwZeFARuQ}
pwn.college{fake_flag_number_27_w9Lv2ZTEU}
pwn.college{fake_flag_number_28_rhiQyYPKUk}
pwn.college{fake_flag_number_29_Tl3xIC92RYc}
pwn.college{fake_flag_number_30_EgCuo6hTYQA}
pwn.college{fake_flag_number_31_SMdRfjm7c}
pwn.college{fake_flag_number_32_NEvMHHCMPpY}
pwn.college{fake_flag_number_33_Y5Nu5sFGYTo}
pwn.college{fake_flag_number_34_xp9xsBAM90}
pwn.college{fake_flag_number_35_mdYl32SLbM}
pwn.college{fake_flag_number_36_JF25mvQQyE}
pwn.college{fake_flag_number_37_XECS3zP7laA}
pwn.college{fake_flag_number_38_ONXeId9SJo}
pwn.college{fake_flag_number_39_GsYKtMPL4iE}
pwn.college{fake_flag_number_40_ZPmJHEMXdlU}
pwn.college{fake_flag_number_41_AteXJKpWUho}
pwn.college{fake_flag_number_42_6uPmolfaYqk}
pwn.college{fake_flag_number_43_nfMaQeeV9w}
pwn.college{fake_flag_number_44_CMf0aHvuUE}
pwn.college{fake_flag_number_45_Ywgh7SVg1nE}
pwn.college{fake_flag_number_46_uSZqHmbhg7E}
pwn.college{fake_flag_number_47_xDNMkwWm5w}
pwn.college{fake_flag_number_48_cq7TQPI58qc}
pwn.college{fake_flag_number_49_1zb8V2tCXEM}
pwn.college{fake_flag_number_50_82JpSC0PbrI}
pwn.college{fake_flag_number_51_ZkhYgR9xEJk}
pwn.college{fake_flag_number_52_Y8IU8FZvyoA}
pwn.college{fake_flag_number_53_1rJdWQvGcoo}
pwn.college{fake_flag_number_54_KGS3zV2ySO4}
pwn.college{fake_flag_number_55_LXkF3yppdZQ}
pwn.college{fake_flag_number_56_rjbqJWiIWw}
pwn.college{fake_flag_number_57_qqebUGK8xo0}
pwn.college{fake_flag_number_58_RVD8N64laMU}
pwn.college{fake_flag_number_59_VfpGQaD4KA}
pwn.college{fake_flag_number_60_OQxXfFzdkSM}
pwn.college{fake_flag_number_61_C6n4QWw30Yk}
pwn.college{fake_flag_number_62_ktKxrOb511A}
pwn.college{fake_flag_number_63_Cx7T5QSVTc}
pwn.college{fake_flag_number_64_dhgnPhACo}
pwn.college{fake_flag_number_65_tHe3UMRMDo}
pwn.college{fake_flag_number_66_TNGHfHvxZw}
pwn.college{fake_flag_number_67_7v0vIHDdDBU}
pwn.college{fake_flag_number_68_9OY0ODfUC5w}
pwn.college{fake_flag_number_69_BRXbMpTpoE}
pwn.college{fake_flag_number_70_sJ2mJbikTzc}
pwn.college{fake_flag_number_71_lfYgdkjW3U}
pwn.college{fake_flag_number_72_9uPTDDgmIhw}
pwn.college{fake_flag_number_73_B9O6bAMOVGs}
pwn.college{fake_flag_number_74_xI4oDaqB9W4}
pwn.college{fake_flag_number_75_PiPFbyebH8}
pwn.college{fake_flag_number_76_T4uHTMUiS8}
pwn.college{fake_flag_number_77_kA0ap0MZA}
pwn.college{fake_flag_number_78_MBej7L9Rkbk}
pwn.college{fake_flag_number_79_zfLinYLB67M}
pwn.college{fake_flag_number_80_TKzh8YQxIk}
pwn.college{fake_flag_number_81_vuiywaZcQ}
pwn.college{fake_flag_number_82_uoPMyVt59eY}
pwn.college{fake_flag_number_83_hM1hFzOzHY}
pwn.college{fake_flag_number_84_xSHKcIIeC1Y}
pwn.college{kc5DrePIejuBZzmex54g_2eggY8.01MwMDOxwCOykjNzEzW}
pwn.college{fake_flag_number_85_QUn40k9r88}
pwn.college{fake_flag_number_86_ziPMRBkQbw}
pwn.college{fake_flag_number_87_H5YvZ66uoo0}
pwn.college{fake_flag_number_88_ZlnscXGMGI}
pwn.college{fake_flag_number_89_Q8gNq8DfyA}
pwn.college{fake_flag_number_90_ZO881jGMjds}
pwn.college{fake_flag_number_91_ddpDX99yk3g}
pwn.college{fake_flag_number_92_ouSot9dPndo}
pwn.college{fake_flag_number_93_KE8OjWFQL0}
pwn.college{fake_flag_number_94_wjEyA7tFS0M}
pwn.college{fake_flag_number_95_VQ2pqG3arU}
pwn.college{fake_flag_number_96_1eUax8g7xdg}
pwn.college{fake_flag_number_97_JRzNJgSguY}
pwn.college{fake_flag_number_98_9cFkSdCpSI}
pwn.college{fake_flag_number_99_YgenUlPy6ok}
pwn.college{fake_flag_number_100_nO5ExlHfJag}
hacker@commands~comparing-files:~$ diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt 
84a85
> pwn.college{kc5DrePIejuBZzmex54g_2eggY8.01MwMDOxwCOykjNzEzW}
```
### New Learning
I learned how to find the difference in text between files.


## Listing files
ls will list files in all the directories provided to it as arguments, and in the current directory if no arguments are provided. In this challenge, we've named /challenge/run with some random name! List the files in /challenge to find it.
### Solve
Listed the files in challenge using ls command and then ran the /challenge/run which was renamed to get the flag.
**Flag:-** pwn.college{gq2HnO53HVmzRLD7FQlSQDWxOzu.QX4IDO0wCOykjNzEzW}
```
hacker@commands~listing-files:~$ ls /challenge/
16302-renamed-run-20356  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/16302-renamed-run-20356
Yahaha, you found me! Here is your flag:
pwn.college{gq2HnO53HVmzRLD7FQlSQDWxOzu.QX4IDO0wCOykjNzEzW}
```
### New Learning
I learned how to list files.


## Touching files
In this level, please create two files: /tmp/pwn and /tmp/college, and run /challenge/run to get your flag
### Solve
Made tmp file in the home directory, made two files in it that is pwn and college using touch command and then ran the /challenge/run to get the flag.
**Flag:-** pwn.college{8y8orOozKa7tNKrJgVB2tNJluRr.QXwMDO0wCOykjNzEzW}
```
hacker@commands~touching-files:~$ ls
Desktop  a
hacker@commands~touching-files:~$ touch /tmp/pwn
hacker@commands~touching-files:~$ touch tmp
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ cd /pwn
bash: cd: /pwn: No such file or directory
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
Success! Here is your flag:
pwn.college{8y8orOozKa7tNKrJgVB2tNJluRr.QXwMDO0wCOykjNzEzW}
```
### New Learning
I learned how to make files using touch command. 


## Removing files
This challenge will create a delete_me file in your home directory! Delete it, then run /challenge/check, which will make sure you've deleted it and then give you the flag
### Solve
Created a delete_me file using touch command, deleted it using rm and then did /challenge/check to check if it was deleted.
**Flag:-** pwn.college{Y6XwHpoYnghuiRPVnjQRMGmCDzl.QX2kDM1wCOykjNzEzW}
```
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{Y6XwHpoYnghuiRPVnjQRMGmCDzl.QX2kDM1wCOykjNzEzW}
```
### New Learning
I learned how to delete a file.


## Moving files
This challenge wants you to move the /flag file into /tmp/hack-the-planet (do it)! When you're done, run /challenge/check, which will check things out and give the flag to you.
### Solve
Used mv command to move the flag to a specified directory and then did /challenge/check to check if it has shifted.
**Flag:-** pwn.college{MzbM3APpzATpHLmWSeF1dDyHUoe.0VOxEzNxwCOykjNzEzW}
```
hacker@commands~moving-files:~$ ls
Desktop  a  tmp
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{MzbM3APpzATpHLmWSeF1dDyHUoe.0VOxEzNxwCOykjNzEzW}
```
### New Learning
I learned how to shift files to specified directory.


## Hidden files
Interestingly, ls doesn't list all the files by default. Linux has a convention where files that start with a . don't show up by default in ls and in a few other contexts. To view them with ls, you need to invoke ls with the -a flag. Go find the flag, hidden as a dot-prepended file in /. 
### Solve
Went to / directory using cd command and did ls -a to get the hidden files and found out the flag and read it using cat.
**Flag:-** pwn.college{Yx3nz7ujBlvI5MMFbNy-9cumWlv.QXwUDO0wCOykjNzEzW}
```
hacker@commands~hidden-files:~$ ls
Desktop  a  tmp
hacker@commands~hidden-files:~$ ls -a
.  ..  .ICEauthority  .bash_history  .cache  .config  .dbus  .local  Desktop  a  tmp
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-115902894710803  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-115902894710803
pwn.college{Yx3nz7ujBlvI5MMFbNy-9cumWlv.QXwUDO0wCOykjNzEzW}
```
### New Learning
I learned how to find hidden files.


## Making directories
Now, go forth and create a /tmp/pwn directory and make a college file in it! Then run /challenge/run, which will check your solution and give you the flag.
### Solve
I first made a directory with the required name using the mkdir command. I then changed the directory to the new directory created by using cd command followed by making the college file in the required directory.
**Flag:-** pwn.college{EjvoaXZtBmFu7iuJ-Cx0cWQsH3A.QXxMDO0wCOykjNzEzW}
```
hacker@commands~making-directories:~$ mkdir /tmp/pwn
hacker@commands~making-directories:/tmp$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{EjvoaXZtBmFu7iuJ-Cx0cWQsH3A.QXxMDO0wCOykjNzEzW}
```
### New Learning
I learned how to make a directory and create a file in it.
