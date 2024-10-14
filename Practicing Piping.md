# Redirecting Output
The ">" inputs your argument/program to the followed file name.
<br>***Commands***
```
echo PWN > COLLEGE
```
***Output***<br>
![{D853AC3F-D865-4A6E-8B0B-1E1DB93C4080}](https://github.com/user-attachments/assets/a5bdbc53-63ab-46e1-b1b7-f64b9dbd7b2f)

# Redirecting more output
You can even run commands to other files using ">"
***Commands***
```
/challenege/run > myflag
cat myflag
```
***Output*** <br>
![{A9B12E94-68DC-4709-981C-C83D9BDD2F87}](https://github.com/user-attachments/assets/4204ab41-b9df-4d81-b0f8-c9ef2321c93a)

# Appending Output
The ">" will delete old ones in order to create a new one. <br>
But by using ">>", it get appended.
<br>***Commands***
```
/challenge/run >> /home/hacker/the-flag
cat /home/hacker/the-flag
```
***Output***<br>
![{2C9773D6-2968-46FA-99B9-F996A99169BE}](https://github.com/user-attachments/assets/88b7ebef-b758-4257-ba37-fd4cfa5746f2)

# Redirecting errors
File Descriptor (FD) is a number that describes the communication channel.<br>
FD 0: Standard Input<br>
FD 1: Standard Output<br>
FD 2: Standard Error<br>
***Commands***
```
/challenge/run > myflag 2> instructions
cat myflag
```
***Output***<br>
![{8B41BF5F-BF22-4663-AE28-EAF3DF0B5B62}](https://github.com/user-attachments/assets/3f944d0f-ee3d-42ed-b079-3139117c813d)

# Redirecting Input
We use *<* to redirect input to programs.
<br>***Commands***
```
echo COLLEGE > PWN
/challenge/run < PWN
```
***Output***<br>
![{1E01E4E9-3FE4-4EDC-BB45-37D45B124C67}](https://github.com/user-attachments/assets/ef6f35b6-77b4-4baa-b7a7-4de70f79783f)

# Grepping stored results
Combination of *grep* and *redirecting*
<br>***Commands***
```
/challenge/run > /tmp/data.txt
grep pwn.college /tmp/data.txt
```
***Output***<br>
![{3DEAF85A-4AB1-457A-B41C-C794182ADEFB}](https://github.com/user-attachments/assets/d1c77a79-fbd3-425b-9ca2-661a0937a18c)

# Grepping live output
Instead of storing the output in a file and grepping it, I can directly grep the flag using *pipe* operator (|).
<br>***Commands***
```
/challenge/run | grep pwn.college
```
***Output***<br>
![{D683640D-1D33-4318-964D-9D70883EF9A5}](https://github.com/user-attachments/assets/cd4fbb6c-bbbe-415b-b266-55e50222e36b)

# Grepping Errors
The pipe (|) operator can only redirect standard output (FD 1) to another program and cannot pipe an error. (Basically, there's no 2|)<br>
We can use >& which redirects a file descriptor to another file descriptor. (Basically redirect error to a fd and then pipe out the error) <br>
***Commands***
```
/challenge/run 2>&1 instructions | grep pwn.college
```
***Output***<br>
![{8988FA73-15FC-4721-9D4C-2EA56B91EBB7}](https://github.com/user-attachments/assets/a4a545bd-5472-4f7a-aa30-9cbfb2ea1277)

# Duplicating piped data with tee
The **tee** commands duplicates the data flowing through pipe to any number of files mentioned.
<br> ***Commands***
```
/challenge/pwn | tee chal_0 | /challenge/college
cat chal_0
/challenge/pwn --secret Yshsb43c | tee chal_0 | /challenge/college
```
***Output***<br>
![{0E843277-AC9B-413B-B985-8D34E1445675}](https://github.com/user-attachments/assets/fd582891-2ea7-4003-b7fa-9fe013682847)

# Writing to multiple programs 
***Commands***
```
/challenge/hack | tee >(/challenge/the) | /challenge/planet
```
***Output***<br>
![{D7B6F21C-C618-4922-934A-2381E9313FCD}](https://github.com/user-attachments/assets/51d9a3ab-4f2b-44dd-b561-b5a7635e4240)
# Star pipping stderr and stdout
***Commands***
```
/challenge/hack > >(/challenge/planet) 2> >(/challenge/the)
```
***Output***<br>
![{DB7EAB18-69CC-4EA8-A6E9-A1B3ABC11387}](https://github.com/user-attachments/assets/bc4b23d1-4e4b-44d9-8d8d-4b46a25620e2)

