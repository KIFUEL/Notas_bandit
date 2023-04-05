## Descripción 
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.

## Hits
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

## Solución
```
En primer lugar abrimos el archivo de wireshark y cargamos la llave que se nos da, recargamos el archivo y vemos que algunas partes del archivo se vuelven de color verde, al momento de entrar en la linea 32 y viendo el encontramos los siguiente:

Pico-Flag: picoCTF{nongshim.shrimp.crackers}\r\n

Y encontramos la bandera
```

## Bandera
picoCTF{nongshim.shrimp.crackers}