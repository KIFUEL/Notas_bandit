## Descripción 
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/9f2d081f12c05202359632c1989e7927/scrambled2.png)

## Hits
[https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)

Think of different ways you can "stack" images
## Solución
```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$ convert scrambled1.png scrambled2.png -compose
add -composite flag.png
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$ ls
flag.png  scrambled1.png  scrambled2.png  values
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$ open scrambled1.png

picoCTF{7188864c}

```

## Bandera
