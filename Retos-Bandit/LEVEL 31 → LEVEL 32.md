# LEVEL 31 → LEVEL 32
# Objetivo

# Datos de acceso al nivel
```
ssh bandit31@bandit.labs.overthewire.org -p 2220
```
# Solución
```
bandit31@bandit:~$ cd /tmp  
bandit31@bandit:/tmp$ ls  
ls: cannot open directory '.': Permission denied  
bandit31@bandit:/tmp$ mkdir git31  
bandit31@bandit:/tmp$ cd git31  
bandit31@bandit:/tmp/git31$ git clone ssh://bandit31-git@localhost/home/bandit31-git/repo  
Cloning into 'repo'...  
Could not create directory '/home/bandit31/.ssh'.  
The authenticity of host 'localhost (127.0.0.1)' can't be established.  
ECDSA key fingerprint is SHA256:98UL0ZWr85496EtCRkKlo20X3OPnyPSB5tB5RPbhczc.  
Are you sure you want to continue connecting (yes/no)? yes  
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).  
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames  
  
bandit31-git@localhost's password:  
remote: Counting objects: 4, done.  
remote: Compressing objects: 100% (3/3), done.  
remote: Total 4 (delta 0), reused 0 (delta 0)  
Receiving objects: 100% (4/4), done.  
bandit31@bandit:/tmp/git31$  
  
bandit31@bandit:/tmp/git31$ cd repo  
bandit31@bandit:/tmp/git31/repo$ git log  
commit df6c5eb91615c6dc9c99f99ca5fd79addfe62594  
Author: Ben Dover <noone@overthewire.org>  
Date:   Tue Oct 16 14:00:46 2018 +0200  
  
    initial commit  
bandit31@bandit:/tmp/git31/repo$ git show df6c5eb91615c6dc9c99f99ca5fd79addfe62594  
commit df6c5eb91615c6dc9c99f99ca5fd79addfe62594  
Author: Ben Dover <noone@overthewire.org>  
Date:   Tue Oct 16 14:00:46 2018 +0200  
  
    initial commit  
  
diff --git a/.gitignore b/.gitignore  
new file mode 100644  
index 0000000..2211df6  
--- /dev/null  
+++ b/.gitignore  
@@ -0,0 +1 @@  
+*.txt  
diff --git a/README.md b/README.md  
new file mode 100644  
index 0000000..0edecc0  
--- /dev/null  
+++ b/README.md  
@@ -0,0 +1,7 @@  
+This time your task is to push a file to the remote repository.  
+  
+Details:  
+    File name: key.txt  
+    Content: 'May I come in?'  
+    Branch: master  
+  
  
bandit31@bandit:/tmp/git31/repo$ ls  
ls  README.md  
bandit31@bandit:/tmp/git31/repo$ cat ls  
commit df6c5eb91615c6dc9c99f99ca5fd79addfe62594  
Author: Ben Dover <noone@overthewire.org>  
Date:   Tue Oct 16 14:00:46 2018 +0200  
  
    initial commit  
  
diff --git a/.gitignore b/.gitignore  
new file mode 100644  
index 0000000..2211df6  
--- /dev/null  
+++ b/.gitignore  
@@ -0,0 +1 @@  
+*.txt  
diff --git a/README.md b/README.md  
new file mode 100644  
index 0000000..0edecc0  
--- /dev/null  
+++ b/README.md  
@@ -0,0 +1,7 @@  
+This time your task is to push a file to the remote repository.  
+  
+Details:  
+    File name: key.txt  
+    Content: 'May I come in?'  
+    Branch: master  
+  
  
bandit31@bandit:/tmp/git31/repo$ cat README.md  
This time your task is to push a file to the remote repository.  
  
Details:  
    File name: key.txt  
    Content: 'May I come in?'  
    Branch: master  
  
bandit31@bandit:/tmp/git31/repo$ nano key.txt  
Unable to create directory /home/bandit31/.nano: Permission denied  
It is required for saving/loading search history or cursor positions.  
  
Press Enter to continue  
  
bandit31@bandit:/tmp/git31/repo$ ls  
key.txt  ls  README.md  
bandit31@bandit:/tmp/git31/repo$ cat key.txt  
May I come in?  
bandit31@bandit:/tmp/git31/repo$  
  
bandit31@bandit:/tmp/git31/repo$ git add key.txt  
The following paths are ignored by one of your .gitignore files:  
key.txt  
Use -f if you really want to add them.  
bandit31@bandit:/tmp/git31/repo$  
  
bandit31@bandit:/tmp/git31/repo$ git add key.txt -f  
bandit31@bandit:/tmp/git31/repo$ git commit  
Unable to create directory /home/bandit31/.nano: Permission denied  
It is required for saving/loading search history or cursor positions.  
  
Press Enter to continue  
  
(*) Añadida linea "Añadido fichero!" en el archivo que nos abre con nano.  
    Guardamos y Cerramos.  
  
Añadido fichero!  
# Please enter the commit message for your changes. Lines starting  
# with '#' will be ignored, and an empty message aborts the commit.  
# On branch master  
# Your branch is up-to-date with 'origin/master'.  
#  
# Changes to be committed:  
#       new file:   key.txt  
#  
# Untracked files:  
#       ls  
#  
  
  
[master 51c50a9] Añadido fichero!  
 1 file changed, 1 insertion(+)  
 create mode 100644 key.txt  
bandit31@bandit:/tmp/git31/repo$  
  
bandit31@bandit:/tmp/git31/repo$ git push  
Could not create directory '/home/bandit31/.ssh'.  
The authenticity of host 'localhost (127.0.0.1)' can't be established.  
ECDSA key fingerprint is SHA256:98UL0ZWr85496EtCRkKlo20X3OPnyPSB5tB5RPbhczc.  
Are you sure you want to continue connecting (yes/no)? yes  
Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).  
This is a OverTheWire game server. More information on http://www.overthewire.org/wargames  
  
bandit31-git@localhost's password:  
Counting objects: 3, done.  
Delta compression using up to 4 threads.  
Compressing objects: 100% (2/2), done.  
Writing objects: 100% (3/3), 328 bytes | 0 bytes/s, done.  
Total 3 (delta 0), reused 0 (delta 0)  
remote: ### Attempting to validate files... ####  
remote:  
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.  
remote:  
remote: Well done! Here is the password for the next level:  
remote: 56a9bf19c63d650ce78e6ec0354ee45e  
remote:  
remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.  
remote:  
To ssh://localhost/home/bandit31-git/repo  
 ! [remote rejected] master -> master (pre-receive hook declined)  
error: failed to push some refs to 'ssh://bandit31-git@localhost/home/bandit31-git/repo'  
bandit31@bandit:/tmp/git31/repo$
```
# Notas Adicionales

# Referencias