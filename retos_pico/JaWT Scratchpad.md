## Objetivo
Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864

## Hints
- Internal server errors can be intentionally returned by this challenge. If you experience one, try clearing your cookies.
- What is that cookie?
- Have you heard of JWT?
## Solución


```
──(kali㉿kali)-[~]
└─$ john token -w=/usr/share/wordlists/rockyou.txt 
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 128/128 SSE2 4x])
Will run 3 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:04 DONE (2023-03-14 11:21) 0.2403g/s 1778Kp/s 1778Kc/s 1778KC/s iloveqmc..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
                        
```
![[Pasted image 20230314092715.png]]
![[Pasted image 20230314092807.png]]
## Notas Adicionales

usando kali y john de riper, y el diccionario que tiene kali, encontramos la palabra usada.
"ilovepico"
ahora con la pagina web https://jwt.io/ y la palabra encontrada volvemos a firmar. y con un editor de cookies se carga la pagina de nuevo.

## Referencias