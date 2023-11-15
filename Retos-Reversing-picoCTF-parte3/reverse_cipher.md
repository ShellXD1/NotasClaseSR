# reverse_cipher
# Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/31c9b832d036a10daeef52d8b4290ef0/rev_this). Can you reverse the flag.
# Solución 
```
cifrado = open('rev_this', 'r').read()
print(cifrado)

flag = ''

for i in range(8, len(cifrado)-1):
        if i & i == 0:
                falg += chr( ord(cifrado[i]) - 5 )
        else:
                flag += chr( ord(cifrado[i]) + 2 )

print(flag)


picoCTF{r3v3rs37ee84d27}
```
# Notas Adicionales

# Referencias