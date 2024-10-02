# Cat
## Cat as a command
**Cat** command is used to read files.<br>
I had to read the file name *flag* from *home directory* to capture the flag.
***Command***
```
cd ..
cat flag
```
***Output***<br>
![{2D0F1784-CD0D-439B-9503-120E86BD7C13}](https://github.com/user-attachments/assets/672ae9ef-17bc-4b0a-a4a0-1a137e510181)
 ## Catting absolute paths
 **Cat** command can be used not just to read files but also for absolute paths from where it has to be read.
 I had to simply use **cat** command with an absolute path */flag*
 ***Command***
 ```
cd ..
cat /flag
```
***Output***<br>
![{249C0648-877C-433E-A679-23DF5DC778D1}](https://github.com/user-attachments/assets/399153c5-b181-451d-8119-854010e9ee69)

## More Catting
Understood that **cat** command can be used with an absolute path, without changing my directory to that file.
simply used **cat** command with the specified absolute path.
***Command***
```
cat /opt/aflplusplus/testcases/flag
```
***Output**<br>
![{F6E02F82-3857-421F-B30A-0598482194C1}](https://github.com/user-attachments/assets/89dddd72-c777-4c32-9456-b05c8a6288e6)

# Grep
**Grep** helps in finding strings in large files. It can search a larger content than **cat** command.
Syntax--> grep STRING_NAME /absolute/path
***Command***
```
grep pwn.college /challenge/data.txt
```
***Output***<br>
![{D15C9E0D-B9ED-4365-834F-7B597059A0D1}](https://github.com/user-attachments/assets/3bd0c4ac-793f-4742-8d57-57871658d23b)




