# Listing Processes
ps = process status/snapshot <br>
It just lists the processes running in the terminal. <br>
**Added Arguments**<br>
*Standard Syntax*<br>
-e (list every process) <br>
-f (list full format) <br>
-ef<br>
*BSD Syntax*<br>
-a (processes of all users) <br>
-u (user readable output) <br>
-x (process that are NOT running in terminal) <br>
-aux <br>
***Commands***
```
ps -ef
ps -aux
(both had the /challenge/run files running)
/challenge/14914-run-29246
```
***Output***<br>
![{AFBC54B8-BD38-4B67-8F1E-6CAECE76A9B1}](https://github.com/user-attachments/assets/6b641d71-d91b-4b8c-b741-4c737244b4df)
 # Killing Processes
 *kill* command is used to terminate the processes.
 (*"sleep number" is a simple command which will run for a the "number" specfic seconds*) <br>
 syntax --> kill PID <br>
 PID is basically the Process IDentifier number. <br>
 ***Commands***
 ```
ps -aux | grep challenge
kill 73
/challenge/run
```
***Output***<br>
![{77E43987-7BB9-4DAB-9317-9698F373555B}](https://github.com/user-attachments/assets/6d0fd53b-1042-42ad-ab76-8188ca708190)

# Interrupting Processes 
Instead of killing the application, it cleanly exits the terminal when *Ctrl+C* is used - INTERRUPTING.
<br> ***Commands***
```
/challenge/run
^C (Ctrl+C)
```
***Output***<br>
![{4C658186-7EE5-4107-8E47-AE931A761C73}](https://github.com/user-attachments/assets/a5027fe0-686c-4afb-a071-7b24b8121900)

# Suspending Processes 
Sometimes instead of interrupting, we can also suspend (pausing) the running processes. <br>
*Ctrl+Z* <br>
***Commands***
```
/challenge/run
^Z (Ctrl+Z)
/challenge/run
```
***Output*** <br>
![{4ECD82C2-5BA9-498D-B85C-5013841ACA57}](https://github.com/user-attachments/assets/dc68de96-f64c-4876-866a-bd2e1da357e3)

# Resuming Processes 
Generally, after suspending the process for some time, we resume it.
<br> The **fg** command is used to resume the particular process. **fg** basically means foregrounding the process.
<br>***Commands***
```
/challenge/run
^Z (Ctrl+Z)
fg /challenge/run
```
***Output***<br>
![{287D67E3-11C5-4878-B4CA-E0023CB35952}](https://github.com/user-attachments/assets/eff022cf-cf26-4a14-94b7-a7aed3928b97)

# Back-grounding Processes
Instead of resuming the process in the foreground(fg), one can also resume it in the background. <br>
By using the **bg** command. <br>
Basically, you can invoke other commands in the shell while this one is running in the background.<br>
in the -ef, if the STAT column has *T* that means it's suspended.
<br>***Commands***
```
/challenge/run
^Z (Ctrl+Z)
bg /challenge/run
```
***Output***<br>
![{4D3A8172-A041-493D-8366-F1B68D88496B}](https://github.com/user-attachments/assets/e6638143-18bf-49af-8a93-a0ae528bf80e)

# Fore-grounding Processes
Using **fg**.
<br>***Commands***
```
/challenge/run
^Z (Ctrl+Z)
bg /challenge/run
fg /challenge/run
```
***Output***<br>
![{DB33A067-EB85-4570-B272-EC1187E1E3B8}](https://github.com/user-attachments/assets/b6c9282c-6d87-4299-9cbb-1b790f9f5989)

# Starting Backgrounding Processes
We can directly start commands in the background without suspending them first. <br>
We just have to add **&** at the end of the command.
<br>***Commands***
```
/challenge/run &
```
***Output***<br>
![{B6A4E749-7803-4ACC-956C-638E937BB57A}](https://github.com/user-attachments/assets/50b9b16c-0157-40f2-939d-69c864a4ff79)

# Process Exit Codes
Every command, every program and every builtin, exits with an exit code when it finishes running.
<br> The code can be used to check if it had run succesfully. 
<br> It can be done by using a special *variable **?***
<br>***Commands***
```
/challenge/get-code
echo $?
/challenge/submit-code 112
```
***Output***<br>
![{620CDE9E-863C-4E0B-A5A5-44BB1C4543EB}](https://github.com/user-attachments/assets/65f82ec0-0cf5-460f-90fb-bc793be80a2f)


