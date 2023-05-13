## Descripción 

We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/48babf8f8c4c6b8baf336680ea5b9ddf/rev_this). Can you reverse the flag.

## Hints



## Solución

![[Pasted image 20230513154736.png]]
```
  GNU nano 6.2                                                               exp.py
cifrado = open ('rev_this','r').read()

print(cifrado)

flag = ''

for i in range (8,len(cifrado)-1):
        if i & 1 == 0:
                flag += chr(ord(cifrado[i]) - 5)

        else:
                flag += chr(ord(cifrado[i]) + 2)

print(flag)
```

```
picoCTF{w1{1wq8/7376j.:}
r3v3rs312528e05
kifuel@DESKTOP-3C07MOG:~/pico /descargas$
kifuel@DESKTOP-3C07MOG:~/pico /descargas$
```

## Bandera
picoCTF{r3v3rs312528e05}