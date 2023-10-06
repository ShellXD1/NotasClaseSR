# An intriguing file

## Objetivo
Se obtuvo un documento txt, y se necesita ver su contenido

## Solución
```python
import base64
import zlib

archivo_codificado = "eJxLy0lM942o9k2syMwtzVUoTk0uLcosqVTILFaozC8tUijNS0ktKi5JzEvJzEtXyE9TKEpNzAEqqAUAgf8WPg=="

# Decodificar en base64
contenido_decodificado = base64.b64decode(archivo_codificado)

# Descomprimir usando zlib
contenido_descomprimido = zlib.decompress(contenido_decodificado)

# Imprimir el contenido descomprimido
print(contenido_descomprimido.decode('utf-8'))

```

el archivo_codificado es el texto que venia en el txt

```bash
└─$ python main.py                       
flagMX{Maximum security is your understanding of reality}
```


## Notas adicionales



## Referencias