## Descripción 
We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.

## Hits
- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

## Solución
```
En primer lugar abrimos el archivo de wireshark y cargamos la llave que se nos da, recargamos el archivo y vemos que algunas partes del archivo se vuelven de color verde, al momento de entrar en la linea 47 en el Seguir secuencia TLS y encontramos los siguiente:

......JFIF..............Exif..MM.*.................J...........R.(...........;.........Z................................picoCTF{honey.roasted.peanuts}......ICC_PROFILE.......lcms....mntrRGB XYZ .........).9acspAPPL...................................

y vemos la bandera

```

## Bandera
picoCTF{honey.roasted.peanuts}