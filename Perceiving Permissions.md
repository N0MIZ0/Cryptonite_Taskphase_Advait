# Changing File Ownership
**ls -l** to check the files and which user is running them. <br>
Having access to *root* is the most powerful thing. <br>
Command to Change Owner = **chown** username filename <br>
chown can only be invoked by the root.
<br>***Commands***
```
cat /flag
```
***Output***<br>
![{76DB2FB6-771E-4172-9920-49C4CF1EF654}](https://github.com/user-attachments/assets/dadb83c5-525b-4674-8be8-3f2e784d54d3)

# Groups and Files
**id** command can be used to check the groups I am in. <br>
**chgrp username filename** is used to change group of a file and then be able to access it.
<br>***Commands***
```
ls -l
chgrp hacker not-the-flag
cat not-the-flag
```
***Output***<br>
![{AC92D7BA-1B41-4E62-8D32-D253BD467E94}](https://github.com/user-attachments/assets/280938aa-267b-4a74-822b-7f0a21f744c1)

# Fun with Group Names
*id** command can be used to check the groups I am in.
<br>***Commands***
```
id
cd ~
chgrp grp17989 not-the-flag
cat not-the-flag
```
***Output***<br>
![{A052C017-1D9C-4BED-9DF7-B20818FB2E7F}](https://github.com/user-attachments/assets/ef926b8b-772d-4c21-8269-21cb6b6feadf)

# Changing Permissions
Important meanings when ls -l is done: <br>
r - user/group/other can read the file (or list the directory) <br>
w - user/group/other can modify the files (or create/delete files in the directory) <br>
x - user/group/other can execute the file as a program (or can enter the directory, e.g., using `cd`) <br>
- - cannot write/execute it. <br>
**chmod** = change mode command used to change the permissions.
<br> **chmod OPTIONS MODE file_name** <br>
Important: <br>
u+r, as above, adds read access to the user's permissions <br>
g+wx adds write and execute access to the group's permissions <br>
o-w removes write access for other users <br>
a-rwx removes all permissions for the user, group, and world <br>
***Commands***
```
cd ~
chmod +r /flag
cat /flag
```
***Output***<br>
![{9653F59F-7983-43DC-BE1A-B3A485709A2C}](https://github.com/user-attachments/assets/ce12fa68-d722-4749-b84d-d083a6a77301)

# Executable Files
Adding the +x to change the file permission to be executable.
<br> ***Commands***
```
chmod +g /challenge/run
/challenge/run
```
***Output***<br>
![{73B2E954-DBF8-47C6-81FA-D19CDF0E0C02}](https://github.com/user-attachments/assets/b1f58aa5-c2fe-4336-9778-ad0051fe9d44)

# Permission Tweaking Practice
Learning: We shall use u,w,o when specfically changing perms for them and just +r/+x/+w when changing perms for self.
<br>***Commands***
```
/challenge/run
chmod g+rww /challenge/pwn
chmod g+x,u+x /challenge/pwn
chmod g-rwx /challenge/pwn
chmod g+rx,u+rwx,o+rx /challenge/pwn
chmod u-rx,g-rwx /challenge/pwn
chmod o-x /challenge/pwn
chmod u+x /challenge/pwn
chmod u-wx /challenge/pwn
chmod +r /flag
cat /flag
```
***Output*** <br>
![{60956A03-F331-4DC4-B10F-CECB9B74C0A6}](https://github.com/user-attachments/assets/fb34bda2-a2c1-42c8-a2e0-eeb13614562b)

# Permissions Setting Practice
Instead of adding/removing, chmod can simply define or set permissions using *=* <br>
Using w=- means setting perms to nothing.
<br>***Commands***
```
chmod u=wx,g=r,o=rwx /challenge/pwn
chmod u=-,g=rw,o=- /challenge/pwn
chmod u=rw,g=rwx,o=x /challenge/pwn
chmod u=x,g=r,o=w /challenge/pwn
chmod u=-,g=-,o=r /challenge/pwn
chmod u=w,g=x,o=rx /challenge/pwn
chmod u=w,g=rx,o=- /challenge/pwn
chmod u=-,g=wx,o=w /challenge/pwn
chmod +r /flag
cat /flag
```
***Output***<br>
![{6D67B031-F1D0-4CD1-904D-D184FDF738F6}](https://github.com/user-attachments/assets/4a238182-3e5b-4ce6-9250-9a602c9ea085)

# The SUID Bit
In many cases, non-root users have to do tasks which require high access and they cant always be shared the password whenever they're working on those specfic programs. <br>
SUID = Set User ID <br>
*when we ls -l, sometime we get rwxs. The s means it's executable with SUID*
<br> Syntax --> chmod u+s [program]
<br> ***Commands***
```
chmod u+s /challenge/getroot
/challenge/getroot
cat /flag
```
***Output***<br>
![{227EF219-73F6-48CA-8459-64082FAA9E59}](https://github.com/user-attachments/assets/45e467ce-145a-4e5a-a932-90cfad995746)
