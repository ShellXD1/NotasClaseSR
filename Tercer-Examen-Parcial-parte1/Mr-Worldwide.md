# Mr-Worldwide
# Objetivo
A musician left us a [message](https://jupiter.challenges.picoctf.org/static/d5570d48262dbba2a31f2a940409ad9d/message.txt). What's it mean?
# Solución 
```
primero reacomode el texto que nos dieron de la siguiente forma:

picoCTF{(
35.028309, 135.753082
46.469391, 30.740883
39.758949, -84.191605
41.015137, 28.979530
24.466667, 54.366669
3.140853, 101.693207
_
9.005401, 38.763611
-3.989038, -79.203560
52.377956, 4.897070
41.085651, -73.858467
57.790001, -152.407227
31.205753, 29.924526}

me di cuenta que son cordenadas, por lo cual voy a google maps y me devuelve sonas de varios paises por lo cual anoto el estado y pais por asi decirlo, de cada ubicacion dandome el siguiente orden:


picoCTF{(
35.028309, 135.753082 Kioto, japon
46.469391, 30.740883  Odesa, ukrania
39.758949, -84.191605 Dayton, ohio
41.015137, 28.979530  Estambul, Turquia
24.466667, 54.366669  Abu Dabi, Emiratos Arabes
3.140853, 101.693207  Kuala lumpur, Malaysia
_
9.005401, 38.763611   Addis Ababa, Etiopia
-3.989038, -79.203560 Loja, ecuador
52.377956, 4.897070   Amsterdam, paises bajos
41.085651, -73.858467 Sleepy hollow, NY
57.790001, -152.407227Kodiak, alaska
31.205753, 29.924526  Alexandria, egipto
} 

viendolo bien con las iniciales de cada estado se forman palabras y intente ponerlas asi en mayusculas como la bandera del reto:

picoCTF{KODIAK_ALASKA}

Nota: Estambul es Istambul en ingles lo cual es la letra que va en el reto, por eso en vez de la e lo cambie por la I, ya que la llave esta en ingles como todos los demas retos.
```
# Notas Adicionales

# Referencias
https://www.google.com.mx/maps/preview