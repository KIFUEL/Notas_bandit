## Descripción 

Connect to this PostgreSQL server and find the flag!`psql -h saturn.picoctf.net -p 55060 -U postgres pico`Password is `postgres`

## Solución
```

kifuel-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 55060 -U postgres pico
Password for user postgres: 
psql: error: connection to server at "saturn.picoctf.net" (13.59.203.175), port 55060 failed: fe_sendauth: no password supplied
kifuel-picoctf@webshell:~$ psql -h saturn.picoctf.net -p 55060 -U postgres pico
Password for user postgres: 
psql (14.5 (Ubuntu 14.5-0ubuntu0.22.04.1), server 15.2 (Debian 15.2-1.pgdg110+1))
WARNING: psql major version 14, server major version 15.
         Some psql features might not work.
Type "help" for help.

pico=# \dt
         List of relations
 Schema | Name  | Type  |  Owner   
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)
pico=# select * from flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)
```


## Bandera
picoCTF{L3arN_S0m3_5qL_t0d4Y_73b0678f}