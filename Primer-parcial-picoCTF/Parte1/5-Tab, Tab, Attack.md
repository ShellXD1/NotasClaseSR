# 5-Tab, Tab, Attack
# Objetivo
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip)
# Solución
```
wget https://mercury.picoctf.net/static/72712e82413e78cc8aa8d553ffea42b0/Addadshashanammu.zip
shellxd-picoctf@webshell:~$ ls -la
total 32
drwxr-xr-x 2 shellxd-picoctf shellxd-picoctf  121 Sep 25 17:19 .
drwxr-xr-x 3 root            root              29 Sep 25 16:29 ..
-rw-r--r-- 1 shellxd-picoctf shellxd-picoctf  220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 shellxd-picoctf shellxd-picoctf 3771 Sep 25 16:29 .bashrc
-rw-r--r-- 1 shellxd-picoctf shellxd-picoctf  807 Sep 25 16:29 .profile
-rw-rw-r-- 1 shellxd-picoctf shellxd-picoctf  167 Sep 25 16:33 .wget-hsts
-rw-rw-r-- 1 shellxd-picoctf shellxd-picoctf 4520 Mar 16  2021 Addadshashanammu.zip
-rw-r--r-- 1 root            root            4443 Sep 25 16:29 README.txt
shellxd-picoctf@webshell:~$ ls -r 
README.txt  Addadshashanammu.zip
shellxd-picoctf@webshell:~$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
shellxd-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt
shellxd-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
shellxd-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onniss
iralis/Ularradallaku$ ls
fang-of-haynekhtnamet
shellxd-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onniss
iralis/Ularradallaku$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_6f332f10}
```
# Notas Adicionales

# Referencias
