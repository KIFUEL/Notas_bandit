## Descripción 
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/205adad23bf9d8303081a0e71c9beab8/dolls.jpg)

## Hits
- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}

## Solución
Como vemos en el reto en las pistas nos dice que podemos esconder archivos en archivos, sabiendo esto utilizamos el comando binwalk -e [nombre_archivo] hasta llegar a algo que nos de la bandera

```
th0rtilla-picoctf@webshell:~/Matry$ ls
dolls.jpg
th0rtilla-picoctf@webshell:~/Matry$ binwalk -e dolls.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378952, uncompressed size: 383937, name: base_images/2_c.jpg
651610        0x9F15A         End of Zip archive, footer length: 22

th0rtilla-picoctf@webshell:~/Matry$ ls
_dolls.jpg.extracted  dolls.jpg
th0rtilla-picoctf@webshell:~/Matry$ cd _dolls.jpg.extracted/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted$ ls
4286C.zip  base_images
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted$ cd base_images/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images$ ls
2_c.jpg
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images$ ls
2_c.jpg  _2_c.jpg.extracted
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted$ ls
2DD3B.zip  base_images
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted$ cd base_images/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images$ ls
3_c.jpg
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images$ binwalk -e 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79807, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images$ ls
3_c.jpg  _3_c.jpg.extracted
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images$ cd _3_c.jpg.extracted/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted$ ls
1E2D6.zip  base_images
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted$ cd base_images/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 63, uncompressed size: 81, name: flag.txt
79785         0x137A9         End of Zip archive, footer length: 22

th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images$ ls
4_c.jpg  _4_c.jpg.extracted
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls
136DA.zip  flag.txt
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt 
picoCTF{96fac089316e094d41ea046900197662}
th0rtilla-picoctf@webshell:~/Matry/_dolls.jpg.extracted/base_images/_2_c.jpg.ex
tracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ 
```

## Bandera
picoCTF{96fac089316e094d41ea046900197662}