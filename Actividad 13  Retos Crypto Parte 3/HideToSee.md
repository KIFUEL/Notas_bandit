## Descripción 
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).

## Hits
Download the image and try to extract it.

## Solución
```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$ steghide extract -sf atbash.jpg
Enter passphrase:
wrote extracted data to "encrypted.txt".
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/escuela$ cat encrypted.txt
krxlXGU{zgyzhs_xizxp_7142uwv9}


```
picoCTF{atbash_crack_7142fde9}
## Bandera
