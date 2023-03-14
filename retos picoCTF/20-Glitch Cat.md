## Objetivo
Our flag printing service has started glitching!`$ nc saturn.picoctf.net 55823`
## Hints

## Solución

```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads$ nc saturn.picoctf.net 55823
'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
^C
C:\Users\Miguel Angel\Downloads>python
Python 3.11.2 (tags/v3.11.2:878ead1, Feb  7 2023, 16:38:35) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> bandera = 'picoCTF{gl17ch_m3_n07_' + chr(0x39) + chr(0x63) + chr(0x34) + chr(0x32) + chr(0x61) + chr(0x34) + chr(0x35) + chr(0x64) + '}'
>>> print(bandera)
picoCTF{gl17ch_m3_n07_9c42a45d}
>>>
```

## Notas Adicionales

## Referencias