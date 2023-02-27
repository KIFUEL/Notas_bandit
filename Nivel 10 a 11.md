## Objetivo
The password for the next level is stored in the file **data.txt**, which contains base64 encoded data
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit10**
ssh:  bandit10@bandit.labs.overthewire.org -p 2220
password: **G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s**
## Solucion

``` bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
bandit10@bandit:~$
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
|base64| uasado para codificar un texto en base 64 con el argumento -d|

The password is: **6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM**

## Referencias