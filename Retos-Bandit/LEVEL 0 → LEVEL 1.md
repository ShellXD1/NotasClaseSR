# LEVEL 0 → LEVEL 1

# Objetivo
The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
# Datos de acceso al nivel
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
bandit0
bandit0
```
# Solución
```
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
# Notas Adicionales
ls → muestra los archivos dentro del directorio
cat → muestra lo que contiene un archivo
# Referencias