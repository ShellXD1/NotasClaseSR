# 3-Nice Netcat
# Objetivo
There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 7449`, but it doesn't speak English...
# Solución
```
shellxd-picoctf@webshell:~$ nc mercury.picoctf.net 7449
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
102 
50 
100 
55 
99 
97 
102 
97 
125 
10
```
Entre a la pagina de cyberchef y utilice la opcion From Decimal para convertir los numeros y obtener la bandera

picoCTF{g00d_k1tty!_n1c3_k1tty!_f2d7cafa}
# Notas Adicionales

# Referencias
https://gchq.github.io/CyberChef/
https://onlinetools.com/ascii/convert-decimal-to-ascii