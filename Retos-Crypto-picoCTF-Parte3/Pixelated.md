# Pixelated

# Objetivo
I have these 2 images, can you make a flag out of them? scrambled1.png scrambled2.png
# Solución 
```
para solucionar este reto realizamos un pequeño programa para unir las dos imagenes utilizando la libreria pillow y numpy.
```

codigo para resolver el reto:
```
from PIL import Image
import numpy as np 

imagen1 = np.asarray(
    Image.open('scrambled1.png')
)

imagen2 = np.asarray(
    Image.open('scrambled2.png')
)
data = imagen1 + imagen2

print(data)

nueva = Image.fromarray(data)

nueva.save('llave.png', 'PNG')
```
picoCTF{2a4d45c7}
# Notas Adicionales

# Referencias