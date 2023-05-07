## Descripción 
What will asm4("picoCTF_f97bb") return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/76ef117df9226a8a9306a8865b14068e/test.S)


## Solución
```
.intel_syntax noprefix
.global asm4
asm4:
		push   ebp
		mov    ebp,esp
		push   ebx
		sub    esp,0x10
		mov    DWORD PTR [ebp-0x10],0x27a
		mov    DWORD PTR [ebp-0xc],0x0
		jmp    asm4+27
		add    DWORD PTR [ebp-0xc],0x1
		mov    edx,DWORD PTR [ebp-0xc]
		mov    eax,DWORD PTR [ebp+0x8]
		add    eax,edx
		movzx  eax,BYTE PTR [eax]
		test   al,al
		jne    asm4+23
		mov    DWORD PTR [ebp-0x8],0x1
		jmp    asm4+138
		mov    edx,DWORD PTR [ebp-0x8]
		mov    eax,DWORD PTR [ebp+0x8]
		add    eax,edx
		movzx  eax,BYTE PTR [eax]
		movsx  edx,al
		mov    eax,DWORD PTR [ebp-0x8]
		lea    ecx,[eax-0x1]
		mov    eax,DWORD PTR [ebp+0x8]
		add    eax,ecx
		movzx  eax,BYTE PTR [eax]
		movsx  eax,al
		sub    edx,eax
		mov    eax,edx
		mov    edx,eax
		mov    eax,DWORD PTR [ebp-0x10]
		lea    ebx,[edx+eax*1]
		mov    eax,DWORD PTR [ebp-0x8]
		lea    edx,[eax+0x1]
		mov    eax,DWORD PTR [ebp+0x8]
		add    eax,edx
		movzx  eax,BYTE PTR [eax]
		movsx  edx,al
		mov    ecx,DWORD PTR [ebp-0x8]
		mov    eax,DWORD PTR [ebp+0x8]
		add    eax,ecx
		movzx  eax,BYTE PTR [eax]
		movsx  eax,al
		sub    edx,eax
		mov    eax,edx
		add    eax,ebx
		mov    DWORD PTR [ebp-0x10],eax
		add    DWORD PTR [ebp-0x8],0x1
		mov    eax,DWORD PTR [ebp-0xc]
		sub    eax,0x1
		cmp    DWORD PTR [ebp-0x8],eax
		jl     asm4+51
		mov    eax,DWORD PTR [ebp-0x10]
		add    esp,0x10
		pop    ebx
		pop    ebp
		ret    


```

usando python para comprobar 

```
#include <stdio.h>

int main(){

    printf("flag: 0x%x\n",asm4("picoCTF_f97bb"));
}
```

```
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/actividad 15$ gcc -m32 -c asm4.S -o asm4.o
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/actividad 15$ gcc -m32 -c solve.c -o solve.o -w
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/actividad 15$ gcc -m32 -o salida.out solve.o asm4.o
kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/actividad 15$ ./salida.out
flag: 0x265
```


## Bandera
flag: 0x265