# The Root and Absolute Path
All the file systems start with **/**.
This style of path is called *absolute path*
# Position thy self and Elsewhere
cd (**C**hanging **D**irectory) command is used to navigate around directories
and change the cwd (**C**urrent **W**orking **D**irectory)
# Relative Path
## Implicit from **/**
Basically it's the relative path to a directory from the cwd. 
Example:
``` 
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
```
*..* refers to the parent directory of the cwd.
## Explicit from **/**
**.** refers right to the same directory
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
# Home-Sweet-Home
*every user has a home directory where all the personal files are stored.* 
the home directory is shortened to **~** for easier usage. 
**~** can be used instead of writing the entire file name of the home directory. 
Also,  
Learnt how to specify a file as an argument.
The argument which is to be executed is known as the *executable*
```
/executable /file_name -----> syntax to specify a file as an argument
"file_name" is basically the location where you want the executable to be executed.
```




