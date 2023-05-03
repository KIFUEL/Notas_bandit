## Descripción 

We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:65352/).

## Solución

El problema nos manda a una pagina web , si damos en mostrar Código fuente veremos algunos archivos , pero si vamos ha  http://saturn.picoctf.net:65352/secret/assets/DX1KYM.jpg vemos una imagen, si nos regresamos hasta secrets/ otra imagen y un texto nos dice que vamos por buen camino. ahora volvemos a mostrar el codigo fuente de la pagina ahroa entramos al CSS  http://saturn.picoctf.net:65352/secret/hidden/file.css, regresamos a hidden , nos mostrara una pagina de login. volvemos a mostrar el Código fuente  ahora entramos al archivo superhidden  http://saturn.picoctf.net:65352/secret/hidden/superhidden/login.css , volvemos a ver mas codigo y ahora lo que hay que hacer es regresar a superhidden nos mostrara una pagina con un texto, damos mostrar codigo fuente y ahora veremos el codigo fuente.


## Bandera

picoCTF{succ3ss_@h3n1c@10n_790d2615}
