# la cifra de 
# Objetivo
I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 32411`.
# Solución
```
usamos el comando que se nos da para el rato y nos devuelve un texto cifrado.

para solucionar este reto entramos a una herramienta web la cual nos ayuda a encontrar la llave para desencritar el codigo, enseguida solo es entrar a la herramienta cyberchef con vigenere para que decodificara el texto.

texto decodificado:

It is interesting how in history people often receive credit for things they did not create

During the course of history, the VigenÃ¨re Cipher has been reinvented many times

It was falsely attributed to Blaise de VigenÃ¨re as it was originally described in 1553 by Giovan Battista Bellaso in his book La cifra del. Sig. Giovan Battista Bellaso 

For the implementation of this cipher a table is formed by sliding the lower half of an ordinary alphabet for an apparently random number of places with respect to the upper halfpicoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}

The first well-documented description of a polyalphabetic cipher however, was made around 1467 by Leon Battista Alberti.

The VigenÃ¨re Cipher is therefore sometimes called the Alberti Disc or Alberti Cipher.

In 1508, Johannes Trithemius invented the so-called tabula recta (a matrix of shifted alphabets) that would later be a critical component of the VigenÃ¨re Cipher.

Bellasoâs second booklet appeared in 1555 as a continuation of the first. The lower halves of the alphabets are now shifted regularly, but the alphabets and the index letters are mixed by means of a mnemonic key phrase, which can be different with each correspondent.

```
picoCTF{b311a50_0r_v1gn3r3_c1ph3r7b996649}
# Notas Adicionales

# Referencias
https://gchq.github.io/CyberChef/
https://www.guballa.de/vigenere-solver