## Objetivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

-   human-readable
-   1033 bytes in size
-   not executable

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit5**
ssh:  bandit5@bandit.labs.overthewire.org -p 2220
password: **lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR**
## Solucion

``` bash

bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ find -readable -size 1033c
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |
|file | muestra el tipo de archivo |
|find| busca archivos dentro del sistema|

Para buscar en el manual se usa man [ nombre del comando ], dentro de la ayuda se puede buscar usando /[palabra a buscar], para pasar a la sigueinte usa N o n
usando Find para buscar el archivo con el parametro -readable para buscar solo archivos con ascii , -size para el tama;o del archivo **find -readable -size 1033c**

ls para ver los archivos que encontre 
usando file ./*  listo todos los archivos y los tipos de archivos 

**cat ./maybehere07/.file2** se abre el archivo de texto 
password del siguiente reto es : **P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU**
## Referencias

[Find human-readable files - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/313442/find-human-readable-files)

[[Nivel 6 a 7]]