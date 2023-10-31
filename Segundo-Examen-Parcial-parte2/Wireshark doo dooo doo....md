# Wireshark doo dooo doo...
# Objetivo
Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ae5b2bc07928fca272ff3900dc9a6cef/shark1.pcapng).
# Solución 
```
Para la solucion de este reto abrimos la captura de paquetes y una vez abierto en wireshark buscamos el que contenga hipertexto que en mi caso fue el numero 823 el paquete que lo transferia le di clic derecho y le di en la parte de follow a http stream, al abrirlo nos da la lalve pero codificada aparentemente en rot13.

utilice cyberchef para decodificar y listo.

picoCTF{p33kab00_1_s33_u_deadbeef}
```
# Notas Adicionales

# Referencias
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=CmN2cGJQR1N7YzMzeG5vMDBfMV9mMzNfaF9xcm5xb3Jyc30K