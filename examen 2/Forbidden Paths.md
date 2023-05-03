## Descripción 

Can you get the flag?Here's the [website](http://saturn.picoctf.net:55287/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Hints



## Solución

en la pagina podemos leer archivos en el directorio usando la barra de búsqueda, por lo tanto cuando ponemos el nombre de alguno de los libros disponibles funciona, la bandera por otro lado esta  afuera en otro directorio.  estamos en `/usr/share/nginx/html/`  por lo que tendremos que salir hasta la raiz para leer la bandera `/flag.txt`. 
escribiendo ../ podremos salir un directorio. son cuatro direcotrios por lo que ../../../../flag.txt   para leer la bandera. 

## Bandera

picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}

