# vault-door-4

# Objetivo
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/09d3002ae349631324a17e2255ae8df2/VaultDoor4.java)
# Solución 
```
para resolver este reto nos damos cuenta que esta la contraseña dentro del codigo codificada en ascii y en octal por lo cual utilice herramientas online para resolver el reto:

106  85   53   116  95   52   95   98  
0x55 0x6e 0x43 0x68 0x5f 0x30 0x66 0x5f
142 131 164 63  163 137 143 61 
'9'  '4'  'f'  '7'  '4'  '5'  '8'  'e' 

la contraseña esta oculta en lo anterior y realice algunas modificaciones pertinentes como quitar comas o en todo caso quitar el 0 de la codificacion octal a texto.

picoCTF{jU5t_4_bUnCh_0f_bYt3s_c194f7458e}
```
# Notas Adicionales

# Referencias
https://www.branah.com/ascii-converter
https://www.browserling.com/tools/octal-to-text