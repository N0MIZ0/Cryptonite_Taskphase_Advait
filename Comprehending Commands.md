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
I simply changed my directory to root and checked for hiddne files. Found a hidden file named *flag*<br>
Then tried running it, but didnt work so I just used the **grep** command to read the flag stored in it. <br>
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


# Epic Filesystem Quest
Terminal kept giving clues by telling me to go to different directories and **list** files and cat the ones with particular names. <br>
Few files were easy to find whereas few were hidden files and hence had to use **ls -a** to find them. There was a certain command which told me to access the file without changind my directory, but I carelessly changed directory resulting in the destruction of the file and restrarting of the challenge. <br>
I then came back to this step on my second try and made sure not to change the directory.<br>
Instead, I direcly listed and **cat** them without **cd**.
<br>
***Commands***
```
  cd /
 ls
 cat DISPATCH
 cd /opt/linux/linux-5.4/include/config/tmpfs
 ls
 cat EVIDENCE
 cd /opt/angr-management/_internal/jedi/third_party/typeshed/third_party/2and3/requests
 ls -a
 cat .TIP
 cd /usr/lib/R/library/splines/libs
 ls
 cat REVELATION
 cd /
 cd /opt/radare2/libr/arch/p/arm/v35/arch-armv7/.git/branches
 cat MEMO
 cd /opt/linux/linux-5.4/tools/testing/selftests/cpu-hotplug
 ls -a
 cat .DOSSIER
 cd /opt/radare2/test/notworking_db/linux-arm
 ls
cat README
ls /opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Scene3D
cat  /opt/angr-management/_internal/PySide6/Qt/qml/QtQuick/Scene3D/ALERT-TRAPPED
cd /usr/include/c++/9/decimal
ls
cat NUGGET

```
***Output***<br>
![{0BAF44E3-5489-4BAF-9489-554793B72AD4}](https://github.com/user-attachments/assets/062c67ba-a7d0-4cd2-bdb4-0a3d6d93a65b)

# Making Directories 
Created a tmp and pwn directory then made a file within named college. Passed the argument **/challenge/run** <br>
***Commands***
```
cd /tmp
mkdir pwn
cd pwn
touch college
/challenge/run
```
***Output*** <br>
![{ED2AB980-D205-4FCC-A46A-19DEB5A070A4}](https://github.com/user-attachments/assets/ed74b5dc-5313-48ad-bf1e-b9fc874860c0)

# Find
**find** and **find -name** will give you specfic locations resepctively.
<br>
Used the **find -name** command and got lots of directories with the name file on it. Used **cat** on each of them till I found the flag.<br>
***Commands***
```
find / -name flag
cat /opt/aflplusplus/frida_mode/test/cache/flag
```
***Output***<br>
![{FBE6D8BC-5392-4AA0-9B7F-76238B0DE29B}](https://github.com/user-attachments/assets/9511e745-19cf-471b-b45b-819ce1140567)
# Linking
Links can be *hard* and *soft*.<br>
![{F25D3A00-4313-4495-9F93-B662C90B104E}](https://github.com/user-attachments/assets/17e62815-112f-492b-abb5-eb00ffe98da9)
<br>
Hardlink is an alternate address that indexes the data.<br>
Softlink contains the original file name, linux understands that this is a symbolic link and then access the file. <br>
Both are same, just the mechanisms are different.<br>
*symlinks* are created with **ln** command and **-s** as argument. <br>
Syntax --> ln -s og_file_path SYMLINK. <br>
**file** command can tell you what type of file it is.
Syntax --> file file_path <br>
***Commands***
```
rm ~/not-the-flag
ln -sf /flag ~/not-the-flag
/challenge/catflag
```

***Output***<br>
![{D50E916C-F67C-4F4B-9795-5FF05A3788AD}](https://github.com/user-attachments/assets/0376f699-0bd6-437d-95c8-c850bb8a7bb8)


