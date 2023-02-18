## Objetivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit6**
ssh:  bandit6@bandit.labs.overthewire.org -p 2220
password: **P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU**
## Solucion

``` bash
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cd /var/lib/dpkg/info

bandit6@bandit:/var/lib/dpkg/info$ cat ./bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:/var/lib/dpkg/info$
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |
|file | muestra el tipo de archivo |
|find| busca archivos dentro del sistema|
|cd| permite movernos dentro de los directorios del sistema|

Para buscar en el manual se usa man [ nombre del comando ], dentro de la ayuda se puede buscar usando /[palabra a buscar], para pasar a la sigueinte usa N o n

usando Find para buscar el archivo con el parametro -user para buscar archivos de un usuario, -group busca archivos de un grupo,  -size para el tama;o del archivo **find -readable -size 1033c** y para terminar se usa el comando 2>/dev/null que nos permite filtrar los mensajes de error.

ls para ver los archivos que encontre 
usando file ./*  listo todos los archivos y los tipos de archivos 

**cat ./maybehere07/.file2** se abre el archivo de texto 
password del siguiente reto es : **z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S**
## Referencias

