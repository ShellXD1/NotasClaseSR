# SQL Direct
# Objetivo
Connect to this PostgreSQL server and find the flag!

Additional details will be available after launching your challenge instance.
# Solución
```
┌──(kali㉿kali)-[~]
└─$ psql -h saturn.picoctf.net -p 61189 -U postgres pico

Password for user postgres: 
psql (15.3 (Debian 15.3-0+deb12u1), server 15.2 (Debian 15.2-1.pgdg110+1))
Type "help" for help.

pico=# \DT
invalid command \DT
Try \? for help.
pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)

pico=# SELECT * FROM FLAGS;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)

```
picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
# Notas Adicionales

# Referencias