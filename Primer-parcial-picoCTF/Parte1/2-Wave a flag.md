# 2-Wave a flag
# Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
# Solución
```
shellxd-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
shellxd-picoctf@webshell:~$ ls
README.txt  flag  warm
shellxd-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
shellxd-picoctf@webshell:~$ chmod +x warm
shellxd-picoctf@webshell:~$ ls -a 
.  ..  .bash_logout  .bashrc  .profile  .wget-hsts  README.txt  flag  warm
shellxd-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```
# Notas Adicionales

# Referencias