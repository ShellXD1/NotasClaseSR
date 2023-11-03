# basic-mod1
# Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/127/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)
# Solución 
```
para resolver este reto realice un pequeño codigo para resolverlo:

import string
message = "128 322 353 235 336 73 198 332 202 285 57 87 262 221 218 405 335 101 256 227 112 140"
alphabet = string.ascii_lowercase + string.digits + "_"
FLAG = "picoCTF{"   
for i in message.split():
        FLAG += alphabet[int(i) % 37]
FLAG += "}"
print("FLAG: ",FLAG)


```
FLAG:  picoCTF{r0und_n_r0und_79c18fb3}
# Notas Adicionales

# Referencias