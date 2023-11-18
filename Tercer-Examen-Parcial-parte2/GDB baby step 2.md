# GDB baby step 2
# Objetivo
Can you figure out what is in the `eax` register at the end of the `main` function? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Debug [this](https://artifacts.picoctf.net/c/520/debugger0_b).
# Solución 
```
Cuando miré el ensamblado, descubrí que no era un proceso muy complicado, así que hice algo de ejercicio mental para traducir el proceso al código Python sin usar un depurador.

var_4 = 123098 
var_c = 607 
var_8 = 0 

while (var_8 < var_c): 
	var_4 = var_4 + var_8 
	var_8 += 1 

print(var_4)

picoCTF{307019}

```
# Notas Adicionales

# Referencias