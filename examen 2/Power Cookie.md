## Descripción 
Can you get the flag?Go to this [website](http://saturn.picoctf.net:65442/) and see what you can discover.

Do you know how to modify cookies?

## Solución

cuando entramos en la pagina podemos ver una frase y un boton, al presionarlo nos manda a otra pagina y dice que no es esta disponible el servicio por el momento.  luego damos click derecho e inspeccionar, se abre las herramientas de desarrollo, luego vamos a la pestaña de almacenamiento y podremos ver una cookie llamada isAdmin con valor de 0, cambiamos ese valor por 1 y recargamos la pagina y listo. bandera se muestra 
## Bandera

picoCTF{gr4d3_A_c00k13_5d2505be}