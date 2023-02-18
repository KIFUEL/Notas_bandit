## Objetivo
The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit7**
ssh:  bandit7@bandit.labs.overthewire.org -p 2220
password: **z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S**
## Solucion

``` bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ nano data.txt

millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |
|file | muestra el tipo de archivo |
|find| busca archivos dentro del sistema|
|cd| permite movernos dentro de los directorios del sistema|

usando nano el editor de texto, y con la funcion de buscar se eoncontro la palabra y a un lado la constrase;a
password del siguiente reto es : **TESKZC0XvTetK0S9xNwm25STk5iWrBvP**
## Referencias