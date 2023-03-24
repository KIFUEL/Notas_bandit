## Objetivo
This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Hints
What is a hex editor?
## Solución


```
File: garden.jpg                                                                                              ASCII Offset: 0x0023056E / 0x00230597 (%100)
00230560  72 65 20 69  73 20 61 20   66 6C 61 67  20 22 70 69                                                                               re is a flag "pi00230570  63 6F 43 54  46 7B 6D 6F   72 65 5F 74  68 61 6E 5F                                                                               coCTF{more_than_00230580  6D 33 33 74  73 5F 74 68   65 5F 33 79  33 33 64 64                                                                               m33ts_the_3y33dd00230590  32 65 45 46  35 7D 22 0A                                                                                                          2eEF5}".

bandera: picoCTF{more_than_m33ts_the_3y33dd2eEF5}
```

## Notas Adicionales

Usando hexedit para abrir la imagen, dentro del programa usando la funcion de buscar por string ponemos pico y ese es el resultado.

## Referencias