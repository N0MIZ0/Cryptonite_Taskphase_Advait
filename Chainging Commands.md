# Chaining with Semicolons
first command; second command
<br>***Commands***
```
/challenge/pwn; /challenge/college
```
***Output***<br>
![{2FAC80C5-885C-40B8-9683-863DE65C4DDB}](https://github.com/user-attachments/assets/1a20a8fa-dfd3-4fd7-b72a-3ea0e6d57930)

# Your First Shell Script
When you gotta run many commands, the chain with semicolon gets long and annoying. <br>
Create a shell script as name.sh and then run it as bash name.sh <br>
use **nano** to create the shell and give it execute perms and then run it.
<br>***Commands***
```
nano x.sh
/challenge/pwn
/challenge/college
^X (CTRL+X)
Y (yes)
*press enter*
bash x.sh
```
***Output***<br>
![{E6B5042D-8F4A-44A3-BE19-48A857A345FE}](https://github.com/user-attachments/assets/116edd3c-39d4-4244-974e-642fb80a91fb)

# Redirecting Script Output
Basically you can redirect even shell outputs using pipe to other commands. <br>
syntax--> bash shellname.sh | commandname
<br>***Commands***
```
nano solve.sh
/challenge/pwn
/challenge/college
^X
Y
*press enter*
bash solve.sh | /challenge/solve
```
***Output***<br>
![{B4637550-DE6E-423C-9694-89862CC8C4E9}](https://github.com/user-attachments/assets/d8118754-9b65-4cc2-ad7f-598a33c2ebc1)

# Executable Shell Scripts
You can give your shell executable perms and then run it without using bash command.
<br> ***Commands***
```
nano solve.sh
/challenge/college
^X
Y
*press enter*
chmod +x solve.sh
./solve.sh
```
***Output***<br>
![{78D4DB52-0F56-4F77-9B1E-FA38DA109F15}](https://github.com/user-attachments/assets/2b5da41d-d527-45ac-8b94-da8455f9137d)

