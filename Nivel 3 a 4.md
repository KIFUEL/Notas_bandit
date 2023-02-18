## Objetivo
The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit3*
ssh:  bandit3@bandit.labs.overthewire.org -p 2220
password: **aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG**
## Solucion

``` bash
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jan 11 19:19 .
drwxr-xr-x 3 root    root    4096 Jan 11 19:19 ..
-rw-r----- 1 bandit4 bandit3   33 Jan 11 19:19 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
bandit3@bandit:~/inhere$
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |

ls para ver los archivos que encontre 
usando **cat .hidden** se abre el archivo de texto 
password del siguiente reto es : **2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe**
## Referencias

[Mostrar los archivos ocultos en Linux (cambiatealinux.com)](https://cambiatealinux.com/mostrar-los-archivos-ocultos-en-linux#:~:text=Desde%20el%20terminal%20con%20el,se%20muestran%20los%20archivos%20ocultos.)
[Cómo ver archivos ocultos Linux terminal - Solvetic](https://www.solvetic.com/tutoriales/article/5846-como-ver-archivos-ocultos-linux-terminal/)





