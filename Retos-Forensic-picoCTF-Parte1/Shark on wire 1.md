#  Shark on wire 1

# Objetivo
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
# Solución
```
Para resolver este reto se utilizo wireshark dado que el archivo era una captura de paquetes, despues buscamos el primer UDP que apareciera y le dimos follow UPD STREAM para encontrar la contraseña
```
picoCTF{StaT31355_636f6e6e}
# Notas Adicionales

# Referencias
