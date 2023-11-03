# Mind your Ps and Qs
# Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
# Solución
```
para resolver este reto necesitamos tener los valores de p y q los cuales los obtenemos factorizando n, para ello utilice la herramienta web factordb para obtener los valores de los cuales el primero es p y el segundo q

```

comandos para ver el archivo:
```
┌──(kali㉿kali)-[~/Documents/retos crypto/Mind-your-ps-and-qs]
└─$ ls
values
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/retos crypto/Mind-your-ps-and-qs]
└─$ cat values                           
Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e: 65537  
```

lo que hice en python3 para resolver el reto:
```
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> from Crypto.Util.number import long_to_bytes
>>> from Crypto.Util.number import inverse
>>> 
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> e = 65537
>>> p = 2434792384523484381583634042478415057961
>>> q = 650809615742055581459820253356987396346063
>>> 
>>> n = p * q
>>> n
1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> tn = (p-1)*(q-1)
>>> d = inverse(e, tn)
>>> m = pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639684640304028661985917
>>> long_to_bytes(m)
b'picoCTF{sma11_N_n0_g0od_73918962}'

```
# Notas Adicionales

# Referencias
http://factordb.com