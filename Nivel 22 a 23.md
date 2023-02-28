## Objetivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit22**
ssh:  bandit22@bandit.labs.overthewire.org -p 2220
password: **WdDozAdTM2z9DiFEQ2mGlwngMfj4EZff**
## Solucion

``` bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt -n 10
c========== the
h;========== password
========== isT
Q!%     6eSvd]
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
e:V&nQutgo
bandit9@bandit:~$
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
|strings| solo muestra los caracteres imprimibles de un archivo de texto|
usando strings data.txt -n 10 , limitando que solo muestre lineas de mas de 10 caracteres 
password del siguiente reto es : **G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s**
## Referencias

