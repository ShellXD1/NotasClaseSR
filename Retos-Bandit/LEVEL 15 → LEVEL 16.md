# LEVEL 15 → LEVEL 16

# Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
# Datos de acceso al nivel
```
ssh bandit15@bandit.labs.overthewire.org -p 2220
bandit15
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
# Solución
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Sep  5 14:21:56 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Sep  5 14:21:56 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Sep  5 14:20:56 2023 GMT; NotAfter: Sep  5 14:21:56 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIERT5t9zANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwOTA1MTQyMDU2WhcNMjMwOTA1MTQyMTU2WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCm
wBiPjdh1RI2h6uD0NBu9weZgCFgUwOM5PTlJzrrbDIG6MojStI6UWFDOGJAGYk/O
3vOKI4XC1r51gsOG+JSQye+9XqlNKVidFm8muvoOQhtCb3vquFm1kn4B5ZlVFPE+
kwN9TB+Vv9vfwXI3HG7o5KBRBZRPKV1KNOU+x3jhjphuXbLOi0PeNHWAyEBHfNEX
Zrz+Zvun+kgq8CmGGp9oMYRfwjmvPaZYQtTH/JUmt7vbsXalAb6oaCHx36GeuEJH
lAoPkI++eVSLJQO7tdtMeNpYKttX1jIjVvMqAKf7Nhx91m7A1mBGjUw8FDjZjhjn
ynORJxJii0nCah3xomyHAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQAx
ECelAuW6irw6S0/rR2vxrL9Oeej7SWiQ1CizTLew+HZRzRQmTwGqmYnSQnMUhCRT
u5vFwP6tnDrUXlSrazBnDve87BMzdECWhauErj9Pt40gLDuSgvLkZWl6P+f8Frb8
FkDUXuqxiq1vZxOcY0gSQpwvLeS06RMi546KNmDt4+Qfvqt4oXRL+882bqgoOqHQ
P/VsqO52CXoAe5rLuhyC/YVnWxIQnjE5EUYkXCd0Zdm7JOzuKbid7FGinAnpzfUz
vaG4FaUl1ITlxUE9xAWiDIDBYZuXUbj8CyipZm+v0ksNPqXYkh/PvK24fyaAeAUL
Yrmp3Qa25oeRjlPTmVTD
-----END CERTIFICATE-----
...
...
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
```
# Notas Adicionales
_openssl_ → puede **crear y gestionar claves y certificados digitales con distintos formatos de datos comunes y llevar a cabo tareas sencillas de autoridad de certificación (CA)**.
# Referencias
- [Secure Socket Layer/Transport Layer Security on Wikipedia](https://en.wikipedia.org/wiki/Secure_Socket_Layer)
- [OpenSSL Cookbook - Testing with OpenSSL](https://www.feistyduck.com/library/openssl-cookbook/online/ch-testing-with-openssl.html)