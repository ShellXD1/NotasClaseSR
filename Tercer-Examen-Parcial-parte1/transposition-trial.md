# transposition-trial
# Objetivo
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/193/message.txt).
# Solución 
```
Al abrir el texto que viene en el archivo vemos que esta encriptado, por lo cual busque un decodificador utilizando la herramienta web Transposition cipher solver.

la descripcion del reto dice que esta dividida en tres bloques por lo cual en la parte donde me pide la llave agrege el numero 3 y para finalizar ordene el resiltado cambiando la posicion del 1 con el 2 y listo regresa lo siguiente:

The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}
```
picoCTF{7R4N5P051N6_15_3XP3N51V3_A9AFB178}
# Notas Adicionales

# Referencias
https://tholman.com/other/transposition/