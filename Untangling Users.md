*There are many users other than just **hacker** and **root.** To access them we use the command **etc/passwd.***


# Becoming root with su
A typical linux does not have /getroot but instead a **su** and **sudo** <br>
su = Switch User command. <br>
*not used to elevate self to root access **anymore*** <br>
su in itself is the command to open a new shell.
<br>***Commands***
```
su
PASSWORD: hack-the-planet
cat /flag
```
***Output***<br>
![{992BC961-44BD-406D-B27C-13E9BBDC6D62}](https://github.com/user-attachments/assets/025c3bbb-adf4-4926-9a27-3fae8f5329ed)

# Other users with su
su will start a new shell, but you can also specify a particular username to switch that user.
<br>***Commands***
```
su zardus
PASSWORD: dont-hack-me
/challenge/run
```
***Output*** <br>
![{3F16AE0A-99EC-47AB-AF98-A708685ADBF1}](https://github.com/user-attachments/assets/5ba8e4aa-a0b1-441f-9c85-9d8720d7a18d)

# Cracking Passwords
passwords used in SU were stored in /etc/passwd but since it's globally accessible it's now changed to /etc/shadow. <br>
In the /etc/shadow:
<br> username : password
<br> If it contains "*" or "!" that means the account is disabled. <br>
Passwords can be "hacked" by the leaked data of /etc/shadow.<br>
john /leaked_file -->(Known as John The Ripper)
<br> ***Commands***
```
cd ~
john /challenge/shadow-leak
su zardus
PASSWORD: aadvark
/challenge/run
```
***Output***<br>
![{F43A44B8-EED4-4AC7-9CED-B256B1037DA4}](https://github.com/user-attachments/assets/09b330b7-9840-4248-ae9a-4779f6573f45)

# Using sudo
su passwords often leak, hence we use sudo.
<br> sudo = SUperuser DO <br>
sudo defaults to running a command as root.<br>
sudo basically gives high elevation. <br>
syntax --> sudo command
<br> ***Commands***
```
sudo cat  /flag
```
***Output***<br>
![{A2C3DD13-BA69-4FB0-951C-694F2EA1A208}](https://github.com/user-attachments/assets/cc4d4356-f076-4aa1-826b-1f9a89b24f3c)


