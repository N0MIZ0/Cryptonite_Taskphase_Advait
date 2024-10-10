# Matching with *
The "*" is a glob which basically outputs the files which match the given argument.
<br> ***Commands***
```
cd /c*
/challenge/run
```
***Output***<br>
![{C1308AEC-2506-4326-A22F-A5BD942C9958}](https://github.com/user-attachments/assets/1297ce78-b061-4c43-a26d-ca662c899c42)

# Matching with ?
The * can match many cheacters, but the "?" can match only upto one character.
<br> ***Commands***
```
cd /?ha??enge
/challenge/run
```
***Output***<br>
![{769A2FFE-59D3-426F-A445-F2331D83E066}](https://github.com/user-attachments/assets/0d089590-0d16-444a-8c27-47b539089ea5)

# Matching with []
A limited form of the "?". It can only match with the single characters of the string within the bracket.
<br> ***Commands***
```
cd /challenge/files
/challenge/run file_[bash]
```
***Output***<br>
![{C4A71D30-CE9D-49CE-B848-64E4DDC230AF}](https://github.com/user-attachments/assets/c16c6d16-976c-4c89-9c37-7c9d4fbc050f)

# Matching paths with []
Exactly the same as previous, just learnt extra that "[]" can also used to match paths.
<br> ***Commands***
```
cd ~
/challenge/run /challenge/files/file_[bash]
```

***Output***<br>
![{F26C19E3-0E23-4FB2-AF8A-5F9050E8E8B8}](https://github.com/user-attachments/assets/9d8cad71-e9d4-478d-b572-7763f8c36eaa)

# Mixing globs
These matching can be interlinked as well. Like []* or []? or ?[] and *[]
<br>***Commands***
```
cd /challenge/files
ls [cep]*
/challenge/run [cep]*
```
***Output***<br>
![{F7748807-8134-492B-80F4-4B6E1950BF46}](https://github.com/user-attachments/assets/0aa6bc79-d7ae-449e-96d3-bf61b7426e6e)

# Exclusionary globbing
Adding a "!" will match all the files which do not match the followed argument. (Similar to !=)<br>
"!" has now been changed to "^" in newer version of shells.
<br> ***Commands***
```
cd /challenge/files
/challenge/run [!pwn]*
```
***Output*** <br>
![{EEB2CA15-D01B-43CF-B7E4-5BC6EF982774}](https://github.com/user-attachments/assets/04e95cfa-9b64-4073-b292-e5ecd903cf74)


```


