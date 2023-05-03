## Descripción 

Go to this [website](http://saturn.picoctf.net:51108/) and see what you can discover.
## Hints





## Solución

Al entrar a la pagina web que nos da el problema podemos ver que hay un login, click derecho y ver Código fuente . una vez ahi vemos que hay un Código en php llamado login, hacemos click para ver que hay, dentro de ese hay otro archivo llamado secure.js entramos y podremos ver las credenciales para iniciar sesión.
```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

Ahora solo hay que usar esas credenciales para entrar en la pagina, cunado ya estemos logeados podremos ver la bandera  

picoCTF{j5_15_7r4n5p4r3n7_05df90c8}

## Bandera
