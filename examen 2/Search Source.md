## Descripción 

The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:50303/)
## Hints



## Solución

entramos en la pagina dada. una vez ahi damos click derecho y ver codigo fuente. entramos en el archivo .CSS y buscamos la palabra pico, listo.
```
     color: #000;
     line-height: 18px;
}
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8} **/
 .carousel-indicators li {
     width: 20px;
     height: 20px;
     border-radius: 11px;
     background-color: #070000;

```


## Bandera
picoCTF{1nsp3ti0n_0f_w3bpag3s_587d12b8}