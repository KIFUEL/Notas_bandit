## Objetivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit2**
ssh:  bandit2@bandit.labs.overthewire.org -p 2220
password: **rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi**
## Solucion

``` bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat 'spaces in this filename'
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |

ls para ver los archivos que encontre 
usando **cat 'spaces in this filename'** se abre el archivo de texto 
password del siguiente reto es : **aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG**
## Referencias

[How to reference filename with spaces in Linux (linuxhint.com)](https://linuxhint.com/reference-filename-with-spaces-linux/)

[[Nivel 3 a 4]]

