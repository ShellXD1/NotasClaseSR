# vault-door-5
# Objetivo
In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/0a53bf0deaba6919f98d8550c35aa253/VaultDoor5.java)
# Solución 
```
para resolver este reto abrimos el codigo y vemos un metodo checkpass con texto extraño el cual da la pista de la decodificacion que tiene la contraseña:

 public boolean checkPassword(String password) {
        String urlEncoded = urlEncode(password.getBytes());
        String base64Encoded = base64Encode(urlEncoded.getBytes());
        String expected = "JTYzJTMwJTZlJTc2JTMzJTcyJTc0JTMxJTZlJTY3JTVm"
                        + "JTY2JTcyJTMwJTZkJTVmJTYyJTYxJTM1JTY1JTVmJTM2"
                        + "JTM0JTVmJTMwJTYyJTM5JTM1JTM3JTYzJTM0JTY2";
        return base64Encoded.equals(expected);
    }
primero junte todo los tres textos los decodifique a base64 primero y despues lo decodifique en URL

picoCTF{c0nv3rt1ng_fr0m_ba5e_64_0b957c4f}
```
# Notas Adicionales

# Referencias
https://encoding.tools