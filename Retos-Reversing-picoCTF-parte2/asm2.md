# asm2
# Objetivo
What does asm2(0x4,0x21) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/7e3eb2f90200ac88126f62ceb4bc3948/test.S)
# Solución
```
┌──(kali㉿kali)-[~/Documents/seguridad/asm2]
└─$ ls
test.S
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/asm2]
└─$ file test.S 
test.S: ASCII text
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/asm2]
└─$ cat test.S 
asm2:
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   sub    esp,0x10
        <+6>:   mov    eax,DWORD PTR [ebp+0xc]
        <+9>:   mov    DWORD PTR [ebp-0x4],eax
        <+12>:  mov    eax,DWORD PTR [ebp+0x8]
        <+15>:  mov    DWORD PTR [ebp-0x8],eax
        <+18>:  jmp    0x509 <asm2+28>
        <+20>:  add    DWORD PTR [ebp-0x4],0x1
        <+24>:  add    DWORD PTR [ebp-0x8],0x74
        <+28>:  cmp    DWORD PTR [ebp-0x8],0xfb46
        <+35>:  jle    0x501 <asm2+20>
        <+37>:  mov    eax,DWORD PTR [ebp-0x4]
        <+40>:  leave  
        <+41>:  ret    

                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/asm2]
└─$ 


```

Cálculos en python
```
┌──(kali㉿kali)-[~]
└─$ python3
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int(0x10)
16
>>> 16/4
4.0
>>> int(0xc)
12
>>> 
>>> 0x4 <= 0xfb46
True
>>> hex(0x21+0x1)
'0x22'
>>> hex(0x4+0x74)
'0x78'
>>> 0x78 <= 0xfb46
True
>>> int(0xfb46 / 0x74)
554
>>> int(0x21)
33
>>> hex(554 + 33)
'0x24b'
>>> hex(555 + 33)
'0x24c'

```

la llave igual que en el anterior reto es el resultado final a secas: 0x24c
# Notas Adicionales

# Referencias
