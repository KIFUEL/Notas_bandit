## Descripción 
Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).

## Hints
`PTR`'s or 'pointers', reference a location in memory where values can be stored.

## Solución


convertimos de hexa a decimal lo que tiene el registro eax 
```
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret

```

En esta línea observamos el numero hexadecimal <+15>: mov DWORD PTR [rbp-0x4],0x9fe1a

0x9fe1a = 654874
por lo tanto la bandera es 

## Bandera
picoCTF{654874}
