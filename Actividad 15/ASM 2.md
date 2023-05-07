## Descripción 
What does asm2(0xb,0x2e) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/717467c8c8b4332ea5873ad8fe7b2dad/test.S)


## Solución
```
.intel_syntax noprefix
.global asm2
asm2:
		push   ebp
		mov    ebp,esp
		sub    esp,0x10
		mov    eax,DWORD PTR [ebp+0xc]
		mov    DWORD PTR [ebp-0x4],eax
		mov    eax,DWORD PTR [ebp+0x8]
		mov    DWORD PTR [ebp-0x8],eax
		jmp    asm2+28
		add    DWORD PTR [ebp-0x4],0x1
		sub    DWORD PTR [ebp-0x8],0xffffff80
		cmp    DWORD PTR [ebp-0x8],0x63f3
		jle    asm2+20
		mov    eax,DWORD PTR [ebp-0x4]
		leave  
		ret    

```

```
#include <stdio.h>
int main(){

    printf("flag: 0x%x\n",asm2(0xb,0x2e));

}
```
flag: 0xf6
usando codigo en c y juntando el respectivo en asm la bandera es 0xf6


