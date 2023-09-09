# LEVEL 14 → LEVEL 15
# Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
# Datos de acceso al nivel
```
ssh bandit14@bandit.labs.overthewire.org -p 2220
bandit14
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
```
# Solución
```
bandit14@bandit:~$ nc localhost 30000 fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
nc: port number invalid: fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
# Notas Adicionales
 _nc_ → es un _comando_ de sistemas Unix que se usa para llevar a cabo diversas tareas de red
# Referencias
- [How the Internet works in 5 minutes (YouTube)](https://www.youtube.com/watch?v=7_LPdttKXPc) (Not completely accurate, but good enough for beginners)
- [IP Addresses](http://computer.howstuffworks.com/web-server5.htm)
- [IP Address on Wikipedia](https://en.wikipedia.org/wiki/IP_address)
- [Localhost on Wikipedia](https://en.wikipedia.org/wiki/Localhost)
- [Ports](http://computer.howstuffworks.com/web-server8.htm)
- [Port (computer networking) on Wikipedia](https://en.wikipedia.org/wiki/Port_(computer_networking))