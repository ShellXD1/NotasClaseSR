# LEVEL 30 → LEVEL 31
# Objetivo
There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
# Datos de acceso al nivel
```
ssh bandit30@bandit.labs.overthewire.org -p 2220
```
# Solución
```
bandit30@bandit:/tmp/jperez3/git30/repo$ git log  
commit 3aa4c239f729b07deb99a52f125893e162daac9e  
Author: Ben Dover <noone@overthewire.org>  
Date:   Tue Oct 16 14:00:44 2018 +0200  
  
    initial commit of README.md  
  
[ Información Documentación Git ]

bandit30@bandit:/tmp/jperez3/git30/repo$ git reflog  
3aa4c23 HEAD@{0}: checkout: moving from master to remotes/origin/master  
3aa4c23 HEAD@{1}: clone: from ssh://bandit30-git@localhost/home/bandit30-git/repo  
bandit30@bandit:/tmp/jperez3/git30/repo$ cd .git  
bandit30@bandit:/tmp/jperez3/git30/repo/.git$ ls  
branches  description  hooks  info  objects      refs  
config    HEAD         index  logs  packed-refs  
  
[ Información Documentación Git ]  
git-pack-refs - Pack heads and tags for efficient repository access  
  
bandit30@bandit:/tmp/jperez3/git30/repo/.git$ cat packed-refs  
# pack-refs with: peeled fully-peeled  
3aa4c239f729b07deb99a52f125893e162daac9e refs/remotes/origin/master  
f17132340e8ee6c159e0a4a6bc6f80e1da3b1aea refs/tags/secret  
  
bandit30@bandit:/tmp/jperez3/git30/repo$ git show f17132340e8ee6c159e0a4a6bc6f80e1da3b1aea  
47e603bb428404d265f59c42920d81e5
```
# Notas Adicionales

# Referencias