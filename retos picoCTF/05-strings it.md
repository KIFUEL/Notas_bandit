## Objetivo
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Hints
strings
## Solución

```
root@DESKTOP-3C07MOG:/home/Compartir archivos# strings strings | grep pico
picoCTF{5tRIng5_1T_7f766a23}
```
Bandera = picoCTF{5tRIng5_1T_7f766a23}
## Notas Adicionales
comando strings mas el grep para solo mostrar las coincidencias
## Referencias