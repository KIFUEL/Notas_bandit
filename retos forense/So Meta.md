## Objetivo
Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).
## Hints
What does meta mean in the context of files?
Ever heard of metadata?
## Solución


```
File: pico_img.png                                                        ASCII Offset: 0x0001A8D2 / 0x0001A8FA (%100)
0001A8D0  74 00 70 69  63 6F 43 54   46 7B 73 30  5F 6D 33 74                                           t.picoCTF{s0_m3t0001A8E0  61 5F 64 38  39 34 34 39   32 39 7D 4B  F2 61 CA 00                                           a_d8944929}K.a..0001A8F0  00 00 00 49  45 4E 44 AE   42 60 82                                                           ...IEND.B`.


bandera: picoCTF{s0_m3ta_d8944929}
```

## Notas Adicionales

Usando hexedit para abrir la imagen, dentro del programa usando la función de buscar por string ponemos pico y ese es el resultado.

## Referencias