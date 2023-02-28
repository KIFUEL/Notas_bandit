## Objetivo

The password for the next level is stored in a file **readme** in the homedirectory. Unfortunately, someone has modified **.bashrc** to log you out when you log in with SSH.

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit18**
ssh:  bandit18@bandit.labs.overthewire.org -p 2220
password: **hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg**
## Solución

``` bash
C:\Users\Miguel Angel\Desktop>ssh  bandit18@bandit.labs.overthewire.org -p 2220 ls
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
readme

C:\Users\Miguel Angel\Desktop>'

C:\Users\Miguel Angel\Desktop>ssh  bandit18@bandit.labs.overthewire.org -p 2220 cat readme
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit18@bandit.labs.overthewire.org's password:
awhqfNnAbc1naukrpqDYcF95h7HoMTrC

C:\Users\Miguel Angel\Desktop>'

```

## Notas Adicionales
Justo después de hacer login se ejecuta un archivo que nos desconecta del servidor, la forma de resolver este problema es concatenando dos comandos para que se ejecuten antes de que nos saquen. primero el comando ssh para hacer login y luego el comando ls para ver lo que hay, lo volvemos a intentar y ejecutamos el ssh con el cuando cat readme y el resultado nos mostrara la constraseña.

password: **awhqfNnAbc1naukrpqDYcF95h7HoMTrC**


## Referencias