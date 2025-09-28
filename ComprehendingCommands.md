# Comprehending commands

## cat: not the pet, but the command
One of the most critical Linux commands is cat. cat is most often used for reading out files, like so:

hacker@dojo:~$ cat /challenge/DESCRIPTION.md
One of the most critical Linux commands is `cat`.
`cat` is most often used for reading out files, like so:
cat will concatenate (hence the name) multiple files if provided multiple arguments. For example:
```
hacker@dojo:~$ cat myfile
This is my file!
hacker@dojo:~$ cat yourfile
This is your file!
hacker@dojo:~$ cat myfile yourfile
This is my file!
This is your file!
hacker@dojo:~$ cat myfile yourfile myfile
This is my file!
This is your file!
This is my file!
```
Finally, if you give no arguments at all, cat will read from the terminal input and output it. We'll explore that in later challenges...

In this challenge, I will copy the flag to the flag file in your home directory (where your shell starts). Go read it with cat!
### Solve
**Flag:-** pwn.college{EhJyLEJqXQ9Pe2pzoYFQp2zjAXr.QXxcTN0wCOykjNzEzW}
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat flag
pwn.college{EhJyLEJqXQ9Pe2pzoYFQp2zjAXr.QXxcTN0wCOykjNzEzW}
```
### New Learning


## catting absolute paths
In the last level, you did cat flag to read the flag out of your home directory! You can, of course, specify cat's arguments as absolute paths:
```
hacker@dojo:~$ cat /challenge/DESCRIPTION.md
In the last level, you did `cat flag` to read the flag out of your home directory!
You can, of course, specify `cat`'s arguments as absolute paths:
...
```
In this directory, I will not copy it to your home directory, but I will make it readable. You can read it with cat at its absolute path: /flag.
FUN FACT: /flag is where the flag always lives in pwn.college, but unlike in this challenge, you typically can't access that file directly.
### Solve
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



```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/share/applications/flag. Go cat it out **without** cding into 
that directory!
hacker@commands~more-catting-practice:~$ cat /usr/share/applications/flag
pwn.college{gfdNlCPHmT-m_XZHiK2owihGYK9.QXwITO0wCOykjNzEzW}
```
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
pwn.college{YZigmbXmuPxGLF2RF8GnT2ppa5q.QX3EDO0wCOykjNzEzW}
```
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
```
hacker@commands~listing-files:~$ ls /challenge/
16302-renamed-run-20356  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/16302-renamed-run-20356
Yahaha, you found me! Here is your flag:
pwn.college{gq2HnO53HVmzRLD7FQlSQDWxOzu.QX4IDO0wCOykjNzEzW}
```
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
```
hacker@commands~removing-files:~$ touch delete_me
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{Y6XwHpoYnghuiRPVnjQRMGmCDzl.QX2kDM1wCOykjNzEzW}
```
```
hacker@commands~moving-files:~$ ls
Desktop  a  tmp
hacker@commands~moving-files:~$ mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{MzbM3APpzATpHLmWSeF1dDyHUoe.0VOxEzNxwCOykjNzEzW}
```
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
```
```
```
```
```
```
```
