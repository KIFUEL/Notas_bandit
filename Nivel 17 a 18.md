## Objetivo
The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit12**
ssh:  bandit12@bandit.labs.overthewire.org -p 2220
password: **JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv**
## Solucion

``` bash
bandit12@bandit:~$ cat data.txt | xxd -r | zcat |bzcat|zcat|tar xO|tar xO|bzcat|tar xO|zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
|tr| rota la palabra como tu quieras|
|"a-zA-Z"| siginifica que voy a rotar las letras de la a - z en minusculas y masyus\
|"n-za-mN-ZA-M"| significa que la n la cambias por z, y la a por m una rotacion de 13 lugares|

password: **wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw**


## Referencias