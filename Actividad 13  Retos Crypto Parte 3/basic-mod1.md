## Descripción 
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/129/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Hits
Do you know what `mod 37` means?

`mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.


## Solución
```
data = open('message.txt').read().split( )
bandera = ''
for n in  data:
        n = int(n) % 37
        if n >= 0  and n <= 25 :
                bandera += chr(n + 65)
        elif n>= 26 and n <= 35:
                bandera += chr(n + 22)
        else :
                bandera += '_'


print('picoCTF{' + bandera + '}')

kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$ python3 numero.py
picoCTF{R0UND_N_R0UND_ADD17EC2}
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$

```


## Bandera
