## Objetivo
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.
## Hints
What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)
## Solución

```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads$ nc jupiter.challenges.picoctf.org 4427 | grep pico
picoCTF{digital_plumb3r_5ea1fbd7}
```
bandera: 
## Notas Adicionales

## Referencias