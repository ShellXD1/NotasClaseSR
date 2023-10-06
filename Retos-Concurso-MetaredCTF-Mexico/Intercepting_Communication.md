# Intercepting Communication

## Objetivo
The security area intercepted a communication from an employee who is selling critical information.
https://ctfd.anuies.mx/files/50cca0db06aeb06da740436ab182d484/attachment.eml?token=eyJ1c2VyX2lkIjoyNDMsInRlYW1faWQiOjEwMCwiZmlsZV9pZCI6MjF9.ZR8AvQ.B4i-EF570QjGI9HUL8r_m2M67zM
## Solución
```bash
flagMX{Details are important}
```
Se descargo el archivo .eml, este es un archivo de tipo de correo, se uso la pagina https://www.encryptomatic.com/viewer/ para observar y extraer el file.7z que habia, tambien se observo que habia un mensaje: The TechDart3 attachment contains the access details.JbZigma will provide access to the password.Submit payment as directed.
la contraseña del file.7z es TechDart3, y el archivo extraido es file.txt, este archivo es una imagen codificada en base64 metida en un txt, para esto escribi un codigo en python:

```python
import base64

# Tu cadena Base64 aquí
texto_encriptado = ""  

# Decodificar Base64
datos_binarios = base64.b64decode(texto_encriptado)

# Guardar en un archivo con la extensión correcta (por ejemplo, ".png")
with open("imagen_original.png", "wb") as archivo_salida:
    archivo_salida.write(datos_binarios)

print("La imagen original se ha guardado como 'imagen_original.png'")

```
La imagen tiene escrita el texto: b216b1NKe0RudXpxcmUgYWFmIGh1dmFyY2JtYn0=
Este esta en Base64 y en Vigenere, la contraseña para VIGENERE es jbZigma

## Notas adicionales
| Comando | Descripción  |
|---------|-----------------------------------------|
| pwd     | Me indica el directorio actual          |
| whoami  | Saber el usuario actual                 |
| cd /    | Me lleva al directorio raiz             |
| ls      | Lista los archivos en la carpeta actual |



## Referencias