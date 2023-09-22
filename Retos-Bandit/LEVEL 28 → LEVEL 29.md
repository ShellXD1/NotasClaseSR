# LEVEL 28 → LEVEL 29
# Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.
# Datos de acceso al nivel
```
ssh bandit28@bandit.labs.overthewire.org -p 2220

```
# Solución
```
bandit28@bandit:/tmp/jperez3/git28/repo$ cat README.md  
# Bandit Notes  
Some notes for level29 of bandit.  
  
## credentials  
  
- username: bandit29  
- password: xxxxxxxxxx  
  
  
(*) con git log podemos ver un log de cambios ejecutados en el repositorio.  
  
bandit28@bandit:/tmp/jperez3/git28/repo$ git log  
commit 073c27c130e6ee407e12faad1dd3848a110c4f95  
Author: Morla Porla <morla@overthewire.org>  
Date:   Tue Oct 16 14:00:39 2018 +0200  
  
    fix info leak  
  
commit 186a1038cc54d1358d42d468cdc8e3cc28a93fcb  
Author: Morla Porla <morla@overthewire.org>  
Date:   Tue Oct 16 14:00:39 2018 +0200  
  
    add missing data  
  
commit b67405defc6ef44210c53345fc953e6a21338cc7  
Author: Ben Dover <noone@overthewire.org>  
Date:   Tue Oct 16 14:00:39 2018 +0200  
  
    initial commit of README.md  
  
(*) con git show y el hash que identifica los cambios "commit" podemos ver los cambios que se han aplicado en esa revisión.  
  
bandit28@bandit:/tmp/jperez3/git28/repo$ git show 186a1038cc54d1358d42d468cdc8e3cc28a93fcb  
commit 186a1038cc54d1358d42d468cdc8e3cc28a93fcb  
Author: Morla Porla <morla@overthewire.org>  
Date:   Tue Oct 16 14:00:39 2018 +0200  
  
    add missing data  
  
diff --git a/README.md b/README.md  
index 7ba2d2f..3f7cee8 100644  
--- a/README.md  
+++ b/README.md  
@@ -4,5 +4,5 @@ Some notes for level29 of bandit.  
 ## credentials  
  
 - username: bandit29  
-- password: <TBD>  
+- password: bbc96594b4e001778eee9975372716b2  
  
bandit28@bandit:/tmp/jperez3/git28/repo$
```
# Notas Adicionales

# Referencias