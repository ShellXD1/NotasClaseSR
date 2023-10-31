# Packets Primer
# Objetivo
Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/194/network-dump.flag.pcap)
# Solución 
```
Utilice wireshark para abrir la captura de paquetes y al tentrar intente darle follow al TCP stream y me dio la llave, solo utilice python para quitar los espacios que traia la llave que me daba wireshark.

┌──(kali㉿kali)-[~]
└─$ python3
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> "p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f }".repleace(' ','')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
AttributeError: 'str' object has no attribute 'repleace'. Did you mean: 'replace'?
>>> "p i c o C T F { p 4 c k 3 7 _ 5 h 4 r k _ c e c c a a 7 f }".replace(' ','')
'picoCTF{p4ck37_5h4rk_ceccaa7f}'
```
picoCTF{p4ck37_5h4rk_ceccaa7f}
# Notas Adicionales

# Referencias