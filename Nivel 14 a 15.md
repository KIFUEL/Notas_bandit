## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit14**
ssh:  bandit14@bandit.labs.overthewire.org -p 2220
password: **fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq**
## Solución

``` bash
bandit14@bandit:~$ ls
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt


```

## Notas Adicionales

password: **jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt**


## Referencias