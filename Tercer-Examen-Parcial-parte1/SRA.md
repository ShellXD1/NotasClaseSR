# SRA
# Objetivo
I just recently learnt about the SRA public key cryptosystem... or wait, was it supposed to be RSA? Hmmm, I should probably check...

Additional details will be available after launching your challenge instance.
# Solución 

Utilice el siguiente programa para resolver el reto:
```
┌──(kali㉿kali)-[~/Documents/SRA]
└─$ cat exp.py 
from pwn import *
import primefac
from itertools import combinations
from Crypto.Util.number import long_to_bytes

#function to generate all the sub lists
def sub_lists (l):
   # initializing empty list
    comb = []

    #Iterating till length of list
    for i in range(1,len(l)+1):
       # Generating sub list
        comb += [list(j) for j in combinations(l, i)]
   # Returning list
    return comb

def divisors(phi):
   print("Give me the divisors of ", phi-1)
  # this is dangerous, but I'm trusting me
   return(eval(input()))

#connect to the server
r = remote('saturn.picoctf.net', 62417)
#get ciphertext
r.recvuntil("anger =")
ciphertext=int(r.recvline())
#get d
r.recvuntil("envy =")
d=int(r.recvline())
print("cipher=",ciphertext)
print("d=",d)
print(r.recvuntil("vainglory?"))
r.recvline()
#since d is e^-1 mod (p-1)*(q-1), d*e=k*(p-1)*(q-1)+1
#so (p-1)*(q-1)*k = d*e-1
factors=divisors(d*65537)
combos = sub_lists(factors)
primes = set()
#try all possible subsets of the list of factors as the factors of (p-1)
for l in combos:
   product = 1
  # multiply them together to get p-1
   for k in l:
      product = product * k
  # if the right length and adding 1 yields a prime, then maybe
   if product.bit_length()==128 and primefac.isprime(product+1):
      primes.add(product+1)
print(primes)
primelist = list(primes)
#try all possible prime pairs
for p in primelist:
   for q in primelist:
      n=p*q
     # decode with this possible n
      plain = pow(ciphertext,d,n)
      try:
         plaintext = long_to_bytes(plain)
        # see if it corresponds to text and if so, try it
         print(plaintext.decode())
         r.sendline(plaintext.decode())
         print(r.recvline())
         print(r.recvline())
         print(r.recvline())
      except:
         continue

```

para que funcione el programa se debe cambiar el puerto por el que te dan al iniciar la instancia en esta parte:
```
#connect to the server
r = remote('saturn.picoctf.net', 62417) #aqui se cambia el numero de puerto
```

Programa funcionando con la modificacion del puerto:
```
┌──(kali㉿kali)-[~/Documents/SRA]
└─$ python3 exp.py
[+] Opening connection to saturn.picoctf.net on port 62417: Done
/home/kali/Documents/SRA/exp.py:26: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("anger =")
/home/kali/Documents/SRA/exp.py:29: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.recvuntil("envy =")
cipher= 36623393553755751332528338731209864353498048386373963657705867657859898827777
d= 28715728161614535858550787030848962434014671947308896830374744950664309128361
/home/kali/Documents/SRA/exp.py:33: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(r.recvuntil("vainglory?"))
b'vainglory?'
Give me the divisors of  1881942676527731836561842929640748451038019555410783171572269659831686827345394856
[2, 2, 2, 29, 167, 263, 2861, 9817, 42019, 275711, 43966897215325140095881, 12909930770748639171302058819426001]
{338089331567806384852335683937964805609, 250091178890942638026463483449920491373, 179086275540437749151468585357649604043}
vhmnKm0CKtSTCpGB
/home/kali/Documents/SRA/exp.py:61: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  r.sendline(plaintext.decode())
b'> vhmnKm0CKtSTCpGB\r\n'
b'Conquered!\r\n'
b'picoCTF{7h053_51n5_4r3_n0_m0r3_b2f9b414}\r\n'
vhmnKm0CKtSTCpGB
[*] Closed connection to saturn.picoctf.net port 62417

```

Al iniciar el programa accede a la instancia y te pide hasta el final que des los divisores de un numero que te da:
```
Give me the divisors of  1881942676527731836561842929640748451038019555410783171572269659831686827345394856
```

en mi caso los divisores fueron los siguientes:
NOTA: recomiendo poner los divisores exactamente en ese formato para la respuesta, es decir, poner los números entre "[ ]" y los números con un espacio después de cada coma. la pagina para obtener los divisores esta al final en referencias, ingresas el numero y das clic en el botón Factor.
```
[2, 2, 2, 29, 167, 263, 2861, 9817, 42019, 275711, 43966897215325140095881, 12909930770748639171302058819426001]
```

después una vez dada la respuesta al final te da la llave y termina la conexión.

picoCTF{7h053_51n5_4r3_n0_m0r3_b2f9b414}
# Notas Adicionales

# Referencias
[Integer factorization calculator (alpertron.com.ar)](https://www.alpertron.com.ar/ECM.HTM)