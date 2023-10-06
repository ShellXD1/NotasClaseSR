# Poor security

# Objetivo
Cybercrime up 600% Due to COVID-19 Pandemic
It is estimated that, worldwide, cyber crimes will cost $10.5 trillion annually by 2025.
The global annual cost of cybercrime is estimated to be $6 trillion per year.
# Solución
```
para solucionar este reto revise los dos archivos txt que proporcionaban para el reto, tras analizarlos me di cuenta de algo importante.

los dos textos eran iguales a exepcion de que algunas palabras y numeros del reto estaban remplazados en uno de los textos con un "~".

al recolectar todas las letras resulto lo siguiente:

ZmxhZ01Ye3Bvb3JzZWN1cml0eX0=

con el signo igual del final recorde que normalmente se trata de una codificacion en base64, con esto en mente entre a la pagina de cyberchef y de ahi obtuve la bandera:

flagMX{poorsecurity}
```
# Notas Adicionales

# Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Wm14aFowMVllM0J2YjNKelpXTjFjbWwwZVgwPQ