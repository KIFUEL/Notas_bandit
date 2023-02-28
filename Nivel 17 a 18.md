## Objetivo
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit18**
ssh:  bandit18@bandit.labs.overthewire.org -p 2220
password: **VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e**
## Solución

``` bash

bandit17@bandit:~$ ls
passwords.new  passwords.old
bandit17@bandit:~$ diff passwords.old passwords.new --color
42c42
< f9wS9ZUDvZoo3PooHgYuuWdawDFvGld2
---
> hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg
bandit17@bandit:~$
```

## Notas Adicionales

con el comando diff podemos comparar dos archivos y mostrar las diferencias de cada uno.

password: **hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg**


## Referencias