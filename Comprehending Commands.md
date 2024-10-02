# Cat
## Cat as a command
**Cat** command is used to read files.<br>
I had to read the file name *flag* from *home directory* to capture the flag.<br>
***Command***
```
cd ..
cat flag
```
***Output***<br>
![{2D0F1784-CD0D-439B-9503-120E86BD7C13}](https://github.com/user-attachments/assets/672ae9ef-17bc-4b0a-a4a0-1a137e510181)
 ## Catting absolute paths
 **Cat** command can be used not just to read files but also for absolute paths from where it has to be read.
 I had to simply use **cat** command with an absolute path */flag* <br>
 ***Command***
 ```
cd ..
cat /flag
```
***Output***<br>
![{249C0648-877C-433E-A679-23DF5DC778D1}](https://github.com/user-attachments/assets/399153c5-b181-451d-8119-854010e9ee69)

## More Catting
Understood that **cat** command can be used with an absolute path, without changing my directory to that file.
simply used **cat** command with the specified absolute path.<br>
***Command***
```
cat /opt/aflplusplus/testcases/flag
```
***Output***<br>
![{F6E02F82-3857-421F-B30A-0598482194C1}](https://github.com/user-attachments/assets/89dddd72-c777-4c32-9456-b05c8a6288e6)

# Grep
**Grep** helps in finding strings in large files. It can search a larger content than **cat** command.<br>
Syntax--> grep STRING_NAME /absolute/path<br>
*CTF always comes with a red highlight over it when you read it using **grep***<br>
***Command***
```
grep pwn.college /challenge/data.txt
```
***Output***<br>
![{D15C9E0D-B9ED-4365-834F-7B597059A0D1}](https://github.com/user-attachments/assets/3bd0c4ac-793f-4742-8d57-57871658d23b)

# Files
## Listing
Directories have lots of files as well as other *directories* within them.<br>
The **ls** command is used to list out all the files within the provided directory as an argument. <br>
If no directory is provided as an argument, then it lists out the files of the current directory.
<br>
Syntax ---> **ls /path**
<br>
Here, I first had to use the **ls** command to list out files from *challenge*<br>
I found 2 files, I could have ran both, but I used **cat** command to check which one was the right file and then ran it. <br><br>
*Just because I am in **/challenge** does not mean can just run **/run**, because adding a **/** itself to a file means that I am in root. Hence have to write the full executable which is **/challenge/run** even when I am already in the **/challenge** directory*<br>
*But, since I am in **/challenge**, I can use just **run** or **./run** instead of using the entire executable* <br>
***Commands***
```
 ls /challenge
 cat /DESCRIPTION.md
 cat /30100-rename-run-21950
 /challenge/30100-rename-run-21950
```
***Output***<br>
![{11B262DC-203C-4071-92B1-EEA1F5AB0570}](https://github.com/user-attachments/assets/a7ab63a1-f38c-4235-9189-3744583815e7)

## Touching 
Blank files can be created by *touching* with **touch** command.
Syntax                                                          ---> touch /absolute/path <br>
Syntax (when you are in the directory you want to add the file) ---> touch <file_name> <br>
***Commands***
```
 cd /tmp
 ls
 touch pwn
 touch college
 /challenge/run
```

***Output***<br>
![{4D0BB335-F55B-49C7-BEE5-65957B4F1276}](https://github.com/user-attachments/assets/436967a1-fb6d-4688-bc32-575b8f5319c1)

## Removing
Use **rm** command to remove files. <br>
Syntax                                                          ---> rm /absolute/path <br>
Syntax (when you are in the directory you want to add the file) ---> rm <file_name> <br>
***Commands***
```
cd ..
rm delete_me
ls
/challenge/check
```
***Output***<br>
![{233FD1BD-75AF-4EF3-BE90-EB57425BCFB8}](https://github.com/user-attachments/assets/918a7977-e86d-4f1a-a3be-3244121bf880)

## Hidden Files
**ls** does not show all files which start with "**.**"<br>
Hence to view them, we add **-a** to the **ls** command.
<br>
Syntax ---> ls -a <br>
***Commands***
```
 cd /
 ls
 ls -a
 .flag-185622975415992
 grep pwn.college /.flag-185622975415992
```
***Output***<br>
![{21F1D1E8-9CC9-412B-AA58-830D22C2643D}](https://github.com/user-attachments/assets/a3293e99-a5eb-467d-ba36-5de5268154bf)






