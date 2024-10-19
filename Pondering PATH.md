# The PATH variable
PATH is a variable that stores bunch of different directly paths. <br>
So in this phase, I just had to blank out the PATH variable and it worked.
<br>***Commands***
```
cd ~
PATH=" "
/challenge/run
```
***Output***<br>
![{F2357583-41A1-44B5-8129-8AA815C6FCAD}](https://github.com/user-attachments/assets/30d4a4af-37ec-4055-b385-75594c5ead1e)

# Setting Path
Sometimes just writing their bare name wont launch if you're in a different directory, but if we can add thier absolute path to PATH variable and from then we can launch them by their bare name.
<br> ***Commands***
```
cd ~
PATH=/challenge/more_commands
/challenge/run
```
***Output***<br>
![{13CDF849-A4D4-4EF6-A586-8B9E1AD138DA}](https://github.com/user-attachments/assets/513df86d-d8a1-4faf-9f3e-bd9f7d6be75f)

# Adding Commands 
use echo $PATH to give out the location of all the paths. <br>
made a variable and read from it, <br>
Since, **read** command is a bulit-in functionality and wont get affected by changing paths.

<br>***Commands***
```
cd ~
$flag
nano win
read flag < /flag
echo $flag
^X (CTRL+X)
Y (yes)
(press enter)
chmod +x win
PATH=/home/hacker
/challenge/run
```
***Output***<br>
![{FD80B8AD-9C32-4DE1-B73D-78C0AE7FEFAD}](https://github.com/user-attachments/assets/f09e2496-5192-4fe7-b5b0-1dc605a6baac)

# Hijacking Commands
Here, I basically have to execute my shell script named **rm** before the terminal executes the real **rm** which will delete my flag.
<br>***Commands***
```
cd ~
$flag
nano rm
read flag < /flag
echo $flag
^X (CTRL+X)
Y (yes)
(press enter)
chmod +x rm
PATH=/home/hacker
/challenge/run
```
***Output***<br>
![{EFF6BAFC-C87C-438E-AD7E-256EBB8109B7}](https://github.com/user-attachments/assets/d7d9c7b6-6335-416f-be4a-79067b0e7306)

