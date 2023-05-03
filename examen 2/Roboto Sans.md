## Descripción 

The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:61304/) out.

## Solución

cuando entramos a la pagina web que nos da el problema debemos entrar al txt robots. 

[saturn.picoctf.net:61304/robots.txt](http://saturn.picoctf.net:61304/robots.txt)

```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/

ZmxhZzEudHh0 = flag1.txt
anMvbXlmaW = js/myfi
anMvbXlmaWxlLnR4dA== = js/myfile.txt
```

parece que hay texto cifrado en base64, usando cyberchef tendremoa el resultado. 
ahora entramos en [saturn.picoctf.net:61304/js/myfile.txt](http://saturn.picoctf.net:61304/js/myfile.txt)
y podremos ver la bandera 

## Bandera

picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}