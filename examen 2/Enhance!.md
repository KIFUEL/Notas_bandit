## Descripción 

Download this image file and find the flag.

-   [Download image file](https://artifacts.picoctf.net/c/100/drawing.flag.svg)

## Solución
```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$ strings drawing.flag.svg | grep {
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$ strings drawing.flag.svg | grep }
         id="tspan3752">c 3 d _ a a b 7 2 9 d d }</tspan></text>
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico$

picoCTf{3nh4nc3d_aab729dd}
```


## Bandera

picoCTf{3nh4nc3d_aab729dd}
