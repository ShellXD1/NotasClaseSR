# 3-PW Crack 1
# Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/12/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/12/level1.flag.txt.enc) in the same directory too.
# Solución
```
shellxd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.py
--2023-09-27 17:48:17--  https://artifacts.picoctf.net/c/12/level1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.71, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 876 [application/octet-stream]
Saving to: 'level1.py'

level1.py                   100%[========================================>]     876  --.-KB/s    in 0s      

2023-09-27 17:48:17 (398 MB/s) - 'level1.py' saved [876/876]

shellxd-picoctf@webshell:~$ ls
README.txt  level1.py
shellxd-picoctf@webshell:~$ python level1.py 
Traceback (most recent call last):
  File "/home/shellxd-picoctf/level1.py", line 13, in <module>
    flag_enc = open('level1.flag.txt.enc', 'rb').read()
FileNotFoundError: [Errno 2] No such file or directory: 'level1.flag.txt.enc'
shellxd-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
--2023-09-27 17:51:20--  https://artifacts.picoctf.net/c/12/level1.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.93, 3.160.5.71, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.93|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 30 [application/octet-stream]
Saving to: 'level1.flag.txt.enc'

level1.flag.txt.enc         100%[========================================>]      30  --.-KB/s    in 0s      

2023-09-27 17:51:20 (15.2 MB/s) - 'level1.flag.txt.enc' saved [30/30]

shellxd-picoctf@webshell:~$ ls
README.txt  level1.flag.txt.enc  level1.py
shellxd-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: ^CTraceback (most recent call last):
  File "/home/shellxd-picoctf/level1.py", line 28, in <module>
    level_1_pw_check()
  File "/home/shellxd-picoctf/level1.py", line 18, in level_1_pw_check
    user_pw = input("Please enter correct password for flag: ")
KeyboardInterrupt

shellxd-picoctf@webshell:~$ nano level1.flag.txt.enc 
shellxd-picoctf@webshell:~$ nano level1.py 
shellxd-picoctf@webshell:~$ python level1.py 
Please enter correct password for flag: 8713
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_1b2fd683}
```
# Notas Adicionales

# Referencias