# LEVEL 19 → LEVEL 20
# Objetivo
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
# Datos de acceso al nivel
```
ssh bandit19@bandit.labs.overthewire.org -p 2220
awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
# Solución
```
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x  2 root     root      4096 Apr 23 18:04 .
drwxr-xr-x 70 root     root      4096 Apr 23 18:05 ..
-rwsr-x---  1 bandit20 bandit19 14876 Apr 23 18:04 bandit20-do
-rw-r--r--  1 root     root       220 Jan  6  2022 .bash_logout
-rw-r--r--  1 root     root      3771 Jan  6  2022 .bashrc
-rw-r--r--  1 root     root       807 Jan  6  2022 .profile
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
# Notas Adicionales
_ls_ → se utiliza para listar archivos o directorios en Linux y otros sistemas operativos basados en Unix.
_cat_ → permite concatenar y mostrar el contenido de archivos.
# Referencias
[setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)