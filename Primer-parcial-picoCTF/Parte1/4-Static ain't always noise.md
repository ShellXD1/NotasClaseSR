# 4-Static ain't always noise
# Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!
# Solución
```
shellxd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
shellxd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
shellxd-picoctf@webshell:~$ ls -la
total 52
drwxr-xr-x 2 shellxd-picoctf shellxd-picoctf   131 Sep 25 17:08 .
drwxr-xr-x 3 root            root               29 Sep 25 16:29 ..
-rw-r--r-- 1 shellxd-picoctf shellxd-picoctf   220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 shellxd-picoctf shellxd-picoctf  3771 Sep 25 16:29 .bashrc
-rw-r--r-- 1 shellxd-picoctf shellxd-picoctf   807 Sep 25 16:29 .profile
-rw-rw-r-- 1 shellxd-picoctf shellxd-picoctf   167 Sep 25 16:33 .wget-hsts
-rw-r--r-- 1 root            root             4443 Sep 25 16:29 README.txt
-rw-rw-r-- 1 shellxd-picoctf shellxd-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 shellxd-picoctf shellxd-picoctf  8376 Mar 16  2021 static
-rwxrwxr-x 1 shellxd-picoctf shellxd-picoctf 10936 Mar 16  2021 warm
shellxd-picoctf@webshell:~$ file static
static: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=277d07901cf99a335a8107fbdd6642d9c6140bb5, not stripped
shellxd-picoctf@webshell:~$ chmod +x static
shellxd-picoctf@webshell:~$ ./static
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
shellxd-picoctf@webshell:~$ strings 
^C
shellxd-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_f5aeda17}
```
# Notas Adicionales

# Referencias
