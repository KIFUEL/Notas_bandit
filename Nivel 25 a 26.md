## Objetivo
Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.

## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit25**
ssh:  bandit25@bandit.labs.overthewire.org -p 2220
password: **p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d**
## Solución

``` bash
 ssh -i bandit26.sshkey bandit26@bandit.labs.overthewire.org -p 2220
The authenticity of host '[bandit.labs.overthewire.org]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names'

  _                     _ _ _   ___   __
 | |                   | (_) | |__ \ / /
 | |__   __ _ _ __   __| |_| |_   ) / /_
 | '_ \ / _` | '_ \ / _` | | __| / / '_ \
 | |_) | (_| | | | | (_| | | |_ / /| (_) |
:e /etc/bandit_pass/bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1

```

## Notas Adicionales
Hay que hacer pequeña la ventana de la terminal, en caso de windows no fucniona tiene que ser en linux
Password : **c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1**
## Referencias
