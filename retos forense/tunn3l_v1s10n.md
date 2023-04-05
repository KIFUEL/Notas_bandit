## Descripción 
We found this [file](https://mercury.picoctf.net/static/09a86202e72dbdb5bf4d1b5d2c6a5b86/tunn3l_v1s10n). Recover the flag.

## Hits
- Weird that it won't display right...

## Solución
```
Vemos el tipo de archivo que es, y el formato hexadecimal del encabezado

th0rtilla-picoctf@webshell:~/tunn3l$ file tunn3l_v1s10n 
tunn3l_v1s10n: data
th0rtilla-picoctf@webshell:~/tunn3l$ xxd tunn3l_v1s10n | head
00000000: 424d 8e26 2c00 0000 0000 bad0 0000 bad0  BM.&,...........
00000010: 0000 6e04 0000 3201 0000 0100 1800 0000  ..n...2.........
00000020: 0000 5826 2c00 2516 0000 2516 0000 0000  ..X&,.%...%.....
00000030: 0000 0000 0000 231a 1727 1e1b 2920 1d2a  ......#..'..) .*
00000040: 211e 261d 1a31 2825 352c 2933 2a27 382f  !.&..1(%5,)3*'8/
00000050: 2c2f 2623 332a 262d 2420 3b32 2e32 2925  ,/&#3*&-$ ;2.2)%
00000060: 3027 2333 2a26 382c 2836 2b27 392d 2b2f  0'#3*&8,(6+'9-+/
00000070: 2623 1d12 0e23 1711 2916 0e55 3d31 9776  &#...#..)..U=1.v
00000080: 668b 6652 996d 569e 7058 9e6f 549c 6f54  f.fR.mV.pX.oT.oT
00000090: ab7e 63ba 8c6d bd8a 69c8 9771 c193 71c1  .~c..m..i..q..q.

Vemos que son datos y tambien nos damos cuenta que empieza con BM, investigando encontramos que es un Bitmap, cambiamos la extension para poder editarlos con el hexeditor.

- En la posicion 0E vemos que esta mal y cambiamos a 28 00 que es 40 en hexadecimal
- En la posicion 0A vemos que esta mal y cambiamos a 28 00 para indicar que ahí empiezan los datos

Ahora que lo corregimos podemos abrirlo y es una imagen, pero no esta la bandera y aparece los siguiente:
notflag{sorry}

Usamos el exiftool para ver los metadatos y vemos que la altura es muy pequeña:
th0rtilla-picoctf@webshell:~/tunn3l$ exiftool tunn3l_v1s10n.bmp 
ExifTool Version Number         : 12.40
File Name                       : tunn3l_v1s10n.bmp
Directory                       : .
File Size                       : 2.8 MiB
File Modification Date/Time     : 2021:03:15 18:24:47+00:00
File Access Date/Time           : 2023:03:30 04:51:19+00:00
File Inode Change Date/Time     : 2023:03:30 04:59:58+00:00
File Permissions                : -rw-rw-r--
File Type                       : BMP
File Type Extension             : bmp
MIME Type                       : image/bmp
BMP Version                     : Windows V3
Image Width                     : 1134
Image Height                    : 306
Planes                          : 1
Bit Depth                       : 24
Compression                     : None
Image Length                    : 2893400
Pixels Per Meter X              : 5669
Pixels Per Meter Y              : 5669
Num Colors                      : Use BitDepth
Num Important Colors            : All
Red Mask                        : 0x27171a23
Green Mask                      : 0x20291b1e
Blue Mask                       : 0x1e212a1d
Alpha Mask                      : 0x311a1d26
Color Space                     : Unknown (,5%()
Rendering Intent                : Unknown (826103054)
Image Size                      : 1134x306
Megapixels                      : 0.347


Volvemos al hexeditor a cambiar la altura hasta encontrar la bandera
- En la posicion 16 que es donde podemos cambiar la altura, lo cambiamos a 40 04

Volvemos a abrir la imagen y ahora si podemos ver la bandera

```

## Bandera
picoCTF{qu1t3_a_v13w_2020}