# WebNet1
# Objetivo

# Solución
```
┌──(kali㉿kali)-[~/Documents/seguridad/WebNet0/WebNet1]
└─$ ls
capture.pcap  picopico.key
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/WebNet0/WebNet1]
└─$ wireshark capture.pcap
 ** (wireshark:66255) 19:57:13.273440 [GUI WARNING] -- FIX Add drag reordering to UAT dialog
 ** (wireshark:66255) 19:59:03.900400 [GUI WARNING] -- QXcbConnection: XCB error: 3 (BadWindow), sequence: 7712, resource id: 19377395, major code: 40 (TranslateCoords), minor code: 0
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/WebNet0/WebNet1]
└─$ ls
capture.pcap  picopico.key  vulture.jpg
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/WebNet0/WebNet1]
└─$ open vulture.jpg      
                                                                                                                   
┌──(kali㉿kali)-[~/Documents/seguridad/WebNet0/WebNet1]
└─$ strings vulture.jpg -n15
picoCTF{honey.roasted.peanuts}
 )/'%'/9339GDG]]}
 )/'%'/9339GDG]]}
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz

```
En esta parte se hace practicamente lo mismo solo que en vez de seguir paquetes seleccionamos el paquete 47 entramos a la seccion file y de ahi a export objects, guardamos el archivo de imagen que viene entre los archivos que viene y ya en terminal proseguimos trabajando con esa imagen.
picoCTF{honey.roasted.peanuts}
# Notas Adicionales

# Referencias
