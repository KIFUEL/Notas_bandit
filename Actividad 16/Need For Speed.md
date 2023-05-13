## Descripción 

The name of the game is [speed](https://www.youtube.com/watch?v=8piqd2BWeGI). Are you quick enough to solve this problem and keep it above 50 mph? [need-for-speed](https://jupiter.challenges.picoctf.org/static/f9abc386dfb1309e687344783f208b20/need-for-speed).

## Hints



## Solución
```

kifuel@DESKTOP-3C07MOG:/mnt/c/Users/Miguel Angel/Downloads/pico/Actividades 16$ gdb need-for-speed
GNU gdb (Ubuntu 12.1-0ubuntu1~22.04) 12.1
Copyright (C) 2022 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
(gdb) info breakpoints
No breakpoints or watchpoints.
(gdb) disassemble main
Dump of assembler code for function main:
   0x000055555540091a <+0>:     push   rbp
   0x000055555540091b <+1>:     mov    rbp,rsp
   0x000055555540091e <+4>:     sub    rsp,0x10
   0x0000555555400922 <+8>:     mov    DWORD PTR [rbp-0x4],edi
   0x0000555555400925 <+11>:    mov    QWORD PTR [rbp-0x10],rsi
   0x0000555555400929 <+15>:    mov    eax,0x0
   0x000055555540092e <+20>:    call   0x5555554008d8 <header>
   0x0000555555400933 <+25>:    mov    eax,0x0
   0x0000555555400938 <+30>:    call   0x55555540082f <set_timer>
   0x000055555540093d <+35>:    mov    eax,0x0
   0x0000555555400942 <+40>:    call   0x55555540087d <get_key>
   0x0000555555400947 <+45>:    mov    eax,0x0
   0x000055555540094c <+50>:    call   0x5555554008ac <print_flag>
   0x0000555555400951 <+55>:    mov    eax,0x0
   0x0000555555400956 <+60>:    leave
   0x0000555555400957 <+61>:    ret
End of assembler dump.
(gdb) br set_timer
Breakpoint 1 at 0x555555400833
(gdb) run
Starting program: /mnt/c/Users/Miguel Angel/Downloads/pico/Actividades 16/need-for-speed
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".
Keep this thing over 50 mph!
============================


Breakpoint 1, 0x0000555555400833 in set_timer ()
(gdb) disassemble set_timer
Dump of assembler code for function set_timer:
   0x000055555540082f <+0>:     push   rbp
   0x0000555555400830 <+1>:     mov    rbp,rsp
=> 0x0000555555400833 <+4>:     sub    rsp,0x10
   0x0000555555400837 <+8>:     mov    DWORD PTR [rbp-0xc],0x1
   0x000055555540083e <+15>:    lea    rsi,[rip+0xffffffffffffffc9]        # 0x55555540080e <alarm_handler>
   0x0000555555400845 <+22>:    mov    edi,0xe
   0x000055555540084a <+27>:    call   0x555555400630 <__sysv_signal@plt>
   0x000055555540084f <+32>:    mov    QWORD PTR [rbp-0x8],rax
   0x0000555555400853 <+36>:    cmp    QWORD PTR [rbp-0x8],0xffffffffffffffff
   0x0000555555400858 <+41>:    jne    0x555555400870 <set_timer+65>
   0x000055555540085a <+43>:    lea    rdi,[rip+0x1a7]        # 0x555555400a08
   0x0000555555400861 <+50>:    call   0x555555400610 <puts@plt>
   0x0000555555400866 <+55>:    mov    edi,0x0
   0x000055555540086b <+60>:    call   0x555555400640 <exit@plt>
   0x0000555555400870 <+65>:    mov    eax,DWORD PTR [rbp-0xc]
   0x0000555555400873 <+68>:    mov    edi,eax
   0x0000555555400875 <+70>:    call   0x555555400620 <alarm@plt>
   0x000055555540087a <+75>:    nop
   0x000055555540087b <+76>:    leave
   0x000055555540087c <+77>:    ret
End of assembler dump.
(gdb) return
Make selected stack frame return now? (y or n) y
#0  0x000055555540093d in main ()
(gdb) disassemble main
Dump of assembler code for function main:
   0x000055555540091a <+0>:     push   rbp
   0x000055555540091b <+1>:     mov    rbp,rsp
   0x000055555540091e <+4>:     sub    rsp,0x10
   0x0000555555400922 <+8>:     mov    DWORD PTR [rbp-0x4],edi
   0x0000555555400925 <+11>:    mov    QWORD PTR [rbp-0x10],rsi
   0x0000555555400929 <+15>:    mov    eax,0x0
   0x000055555540092e <+20>:    call   0x5555554008d8 <header>
   0x0000555555400933 <+25>:    mov    eax,0x0
   0x0000555555400938 <+30>:    call   0x55555540082f <set_timer>
=> 0x000055555540093d <+35>:    mov    eax,0x0
   0x0000555555400942 <+40>:    call   0x55555540087d <get_key>
   0x0000555555400947 <+45>:    mov    eax,0x0
   0x000055555540094c <+50>:    call   0x5555554008ac <print_flag>
   0x0000555555400951 <+55>:    mov    eax,0x0
   0x0000555555400956 <+60>:    leave
   0x0000555555400957 <+61>:    ret
End of assembler dump.
(gdb) continue
Continuing.
Creating key...
Finished
Printing flag:
PICOCTF{Good job keeping bus #190ca38b speeding along!}
[Inferior 1 (process 1314) exited normally]
(gdb)


```


## Bandera

PICOCTF{Good job keeping bus #190ca38b speeding along!}