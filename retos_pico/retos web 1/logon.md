## Objetivo
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/44573/` ([link](https://jupiter.challenges.picoctf.org/problem/44573/)) or http://jupiter.challenges.picoctf.org:44573
## Hints
Hmm it doesn't seem to check anyone's password, except for Joe's?
## Solución

La pagina web tiene un login con el cual puedes entrar con cualquier combination de usuario y passwords, una vez adentro podemos ver un mensaje diciendo que no podemos ver la bandera. usando la extension de editar las cookies nos daremos cuenta que hay una cookie llamada admin, con el valor false, si cambiamos y guardamos esa cookie con el valor True entonces recargamos la pagina y tendremos la bandera.

```
picoCTF{th3_c0nsp1r4cy_l1v3s_0c98aacc}
```


## Notas Adicionales



## Referencias