## Objetivo

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit19**
ssh:  bandit19@bandit.labs.overthewire.org -p 2220
password: **awhqfNnAbc1naukrpqDYcF95h7HoMTrC**
## Solución

``` bash
bandit19@bandit:~$ ls
bandit20-do
bandit19@bandit:~$ ./bandit20-do
Run a command as another user.
  Example: ./bandit20-do id
  bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
	VxCazJaVykI6W36BkBU0mJTCM8rR95XT

```

## Notas Adicionales
El programa bandit20-do hace comandos en nombre de otro usuario , en este caso al usuario 20, con esto podemos entrar a las carpetas con los passwords de cada uno de los usuario para ver el password

password: **VxCazJaVykI6W36BkBU0mJTCM8rR95XT**


## Referencias