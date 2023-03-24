## Objetivo
This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Hints
How do operating systems know what kind of file it is? (It's not just the ending!
Make sure to submit the flag as picoCTF{XXXXX}
## Solución

```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/forenses$ ls
capture.pcap  flag.txt  garden.jpg  pico_img.png
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/forenses$ mv flag.txt flag.png
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/forenses$ ls
capture.pcap  flag.png  garden.jpg  pico_img.png
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/forenses$ open flag.png

bandera picoCTF{now_you_know_about_extensions}
```

## Notas Adicionales

## Referencias