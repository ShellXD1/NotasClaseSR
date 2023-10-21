# shark on wire 2

# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/b506393b6f9d53b94011df000c534759/capture.pcap). Recover the flag that was pilfered from the network.
# Solución
```
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ ls
capture.pcap
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ file capture.pcap  
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ wireshark capture.pcap 
 
^Z
zsh: suspended  wireshark capture.pcap
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ python3                        
Python 3.11.4 (main, Jun  7 2023, 10:13:09) [GCC 12.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> chr(112)
'p'
>>> chr(105)
'i'
>>> chr(99)
'c'
>>> chr(111)
'o'
>>> chr(67)
'C'
>>> 
zsh: suspended  python3
                                                                                                                                                                                                                                            
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ nano exp.py
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ python3 -m pip install scapy   
Defaulting to user installation because normal site-packages is not writeable
DEPRECATION: Loading egg at /usr/local/lib/python3.11/dist-packages/PySoundFile-0.9.0.post1-py3.11.egg is deprecated. pip 23.3 will enforce this behaviour change. A possible replacement is to use pip for package installation..
DEPRECATION: Loading egg at /usr/local/lib/python3.11/dist-packages/sstv-0.1-py3.11.egg is deprecated. pip 23.3 will enforce this behaviour change. A possible replacement is to use pip for package installation..
Requirement already satisfied: scapy in /usr/lib/python3/dist-packages (2.5.0)
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ python3 exp.py                           
Traceback (most recent call last):
  File "/home/kali/Documents/seguridad/shark on wire 2/exp.py", line 4, in <module>
    packets - rdpcap('capture.pcap')
    ^^^^^^^
NameError: name 'packets' is not defined
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ python3 exp.py                           
Traceback (most recent call last):
  File "/home/kali/Documents/seguridad/shark on wire 2/exp.py", line 9, in <module>
    if udp in p and p[UDP].dport == 22:
       ^^^
NameError: name 'udp' is not defined
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/seguridad/shark on wire 2]
└─$ python3 exp.py
picoCTF{p1LLf3r3d_data_v1a_st3g0}
```
Codigo del exploit(exp.py):
```
rom scapy.all import *

packets = rdpcap('capture.pcap')

flag = ''

for p in packets:
        if UDP in p and p[UDP].dport == 22:
                if p[UDP].sport > 5000:
                        flag += chr(p[UDP].sport - 5000)
print(flag)

```
picoCTF{p1LLf3r3d_data_v1a_st3g0}
# Notas Adicionales

# Referencias
