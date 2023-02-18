## Objetivo
The password for the next level is stored in a file called **-** located in the home directory

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit1**
ssh:  bandit1@bandit.labs.overthewire.org -p 2220
password: **NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL**
## Solucion

``` bash
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
| cat | muestra el contenido del archivo |

ls para ver los archivos que encontre 
usando **cat ./-** se abre el archivo de texto 
password del siguiente reto es : **rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi**
## Referencias

[linux - How to open a "-" dashed filename using terminal? - Stack Overflow](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)

