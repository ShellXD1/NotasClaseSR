# 5- PW Crack 3
# Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
# Solución
```
shellxd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.py
--2023-09-27 18:22:19--  https://artifacts.picoctf.net/c/18/level3.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.42, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1337 (1.3K) [application/octet-stream]
Saving to: 'level3.py'

level3.py                   100%[========================================>]   1.31K  --.-KB/s    in 0s      

2023-09-27 18:22:19 (38.4 MB/s) - 'level3.py' saved [1337/1337]

shellxd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
--2023-09-27 18:22:34--  https://artifacts.picoctf.net/c/18/level3.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.18, 3.160.5.71, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level3.flag.txt.enc'

level3.flag.txt.enc         100%[========================================>]      31  --.-KB/s    in 0s      

2023-09-27 18:22:34 (941 KB/s) - 'level3.flag.txt.enc' saved [31/31]

shellxd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/18/level3.hash.bin
--2023-09-27 18:22:57--  https://artifacts.picoctf.net/c/18/level3.hash.bin
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.42, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 16 [application/octet-stream]
Saving to: 'level3.hash.bin'

level3.hash.bin             100%[========================================>]      16  --.-KB/s    in 0s      

2023-09-27 18:22:57 (16.5 MB/s) - 'level3.hash.bin' saved [16/16]
shellxd-picoctf@webshell:~$ ls
README.txt  level3.flag.txt.enc  level3.hash.bin  level3.py
shellxd-picoctf@webshell:~$ nano level3.py 
shellxd-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 1ea2
That password is incorrect
shellxd-picoctf@webshell:~$ nano level3.py 
shellxd-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 8799
That password is incorrect
shellxd-picoctf@webshell:~$ nano level3.py 
shellxd-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: d3ab
That password is incorrect
shellxd-picoctf@webshell:~$ nano level3.py 
shellxd-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: acaf
That password is incorrect
shellxd-picoctf@webshell:~$ nano level3.py 
shellxd-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
shellxd-picoctf@webshell:~$
```
# Notas Adicionales

# Referencias