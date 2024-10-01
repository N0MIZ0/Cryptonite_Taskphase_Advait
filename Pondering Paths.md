# The Root and Absolute Path
All the file systems start with **/**. <br>
This style of path is called *absolute path*<br>
***Command***
```
1. /pwn
2. /challenge/run
```
***Output*** <br>
![{C72A1A09-3B99-40B4-95FA-E0C8A87356E5}](https://github.com/user-attachments/assets/fed94f0d-bc48-4adb-8500-d44ee3d6a92f)
![{216A34A5-A974-4122-B672-4564BACA7EB3}](https://github.com/user-attachments/assets/82897019-59e6-470c-acc8-c0552228fee4)


# Position thy self and Elsewhere
cd (**C**hanging **D**irectory) command is used to navigate around directories
and change the cwd (**C**urrent **W**orking **D**irectory)<br>
***Commmand***
```
1. cd /sys
   /challenge/run
2. cd /usr/share/zoneinfo/posix/Asia
  /challenge/run
3. cd/var/log
  /challenge/run
```

***Output***<br>
![{22BC1206-781D-41F7-8542-D2CA9F7FB37A}](https://github.com/user-attachments/assets/f216c450-5bf9-4acc-b1c0-154627eacccb)
![{140E47DD-191F-415B-8539-8C33B0FD686B}](https://github.com/user-attachments/assets/34c28a19-9b88-4783-8c8e-1cf1f9772e7b)
![{AE701403-A3C1-44C5-AD4E-28E4C5071509}](https://github.com/user-attachments/assets/ee701937-01a3-4e5e-81d5-f99d26f88282)



# Relative Path
## Implicit from **/**
Basically it's the relative path to a directory from the cwd. <br>
Example:
``` 
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
```
*..* refers to the parent directory of the cwd.
***Commmand***
```
1. cd ..
   challenge/run
2. cd /challenge
   ./run

```
***Output***
![{78B631A2-209B-4876-BE49-33E90EF85F13}](https://github.com/user-attachments/assets/75c328fe-291c-47a4-8965-de6063be20fd)
![{7CE76D45-270C-423D-847F-2B1556BFADF4}](https://github.com/user-attachments/assets/6896fdc6-6f93-428e-abc1-4526eeb5dca2)




## Explicit from **/**
**.** refers right to the same directory. <br>
Example: (Following Absolute Paths are same)
```
/abc
/abc/.
/./abc
```
Example: (Following Relative Paths are same)
```
abc/././././
./abc
abc
```
***Commmand***
```
cd ..
./challenge/run

```
***Output***
![{BAFB1803-8EAF-47D4-81B1-41D9B09EB369}](https://github.com/user-attachments/assets/fdcdd531-0bdb-4565-93c5-c5c1c631e1f5)

# Home-Sweet-Home
*every user has a home directory where all the personal files are stored.* <br>
the home directory is shortened to **~** for easier usage. 
**~** can be used instead of writing the entire file name of the home directory. 
Also,<br>
Learnt how to specify a file as an argument.
The argument which is to be executed is known as the *executable*
```
/executable /file_name -----> syntax to specify a file as an argument
"file_name" is basically the location where you want the executable to be executed.
```
***Command****
```
/challenge/run ~/a
```
***Output***
![image](https://github.com/user-attachments/assets/280bba08-54f3-4e77-a00c-6b091cd94791)




