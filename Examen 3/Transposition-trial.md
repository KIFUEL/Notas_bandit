## Descripción 
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/192/message.txt).

## Hints



## Solución

el archivo txt que descargamos contiene esl siguiente texto
heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2

como podemos ver, la bandera empiza con pico por lo que esta en desorden con el sigueinte codigo en python podemos reordenar 

```
ctxt = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2"
ptxt = ""
 
for i in range(len(ctxt)):
    if i % 3 == 0:
        ptxt = ptxt + ctxt[i+2] + ctxt[i]
    elif i % 3 == 2:
        pass
    else:
        ptxt = ptxt + ctxt[i]
 
print(ptxt)
```



## Bandera

picoCTF{7R4N5P051N6_15_3XP3N51V3_109AB02E}
