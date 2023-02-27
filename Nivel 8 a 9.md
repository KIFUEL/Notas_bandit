## Objetivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit8**
ssh:  bandit8@bandit.labs.overthewire.org -p 2220
password: **TESKZC0XvTetK0S9xNwm25STk5iWrBvP**
## Solucion

``` bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
|sort| ordena la salida de un archivo|
|uniq | cuenta, ordena y muestra solo las lineas unicas|

uniq -u muestra solo las lineas unicas dentro de un archivo de texto 
password del siguiente reto es : **EN632PlfYiZbn3PhVK3XOGSlNInNE00t**
## Referencias
[[Nivel 9 a 10]]