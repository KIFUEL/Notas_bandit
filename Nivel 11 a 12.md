## Objetivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit11**
ssh:  bandit11@bandit.labs.overthewire.org -p 2220
password: **6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM**
## Solucion

``` bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr "a-zA-Z" "n-za-mN-ZA-M"
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$ 
```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
|tr| rota la palabra como tu quieras|
|"a-zA-Z"| siginifica que voy a rotar las letras de la a - z en minusculas y masyus\
|"n-za-mN-ZA-M"| significa que la n la cambias por z, y la a por m una rotacion de 13 lugares|

password: **JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv**


## Referencias