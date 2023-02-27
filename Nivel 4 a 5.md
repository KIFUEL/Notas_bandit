## Objetivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit4**
ssh:  bandit4@bandit.labs.overthewire.org -p 2220
password: **2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe**
## Solucion

``` bash
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$

```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |
|file | muestra el tipo de archivo |


ls para ver los archivos que encontre 
usando file ./*  listo todos los archivos y los tipos de archivos 

**cat ./-file07** se abre el archivo de texto 
password del siguiente reto es : **lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR**
## Referencias

[Find human-readable files - Unix & Linux Stack Exchange](https://unix.stackexchange.com/questions/313442/find-human-readable-files)

[[Nivel 5 a 6]]