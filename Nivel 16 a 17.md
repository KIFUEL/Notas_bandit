## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit16**
ssh:  bandit16@bandit.labs.overthewire.org -p 2220
password: **JQttfApK4SeyHwDlI9SXGR50qclOAil1**
## Solucion

``` bash
bandit16@bandit:~$ nmap -p 31000-32000 localhost
Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-23 14:20 UTC
Nmap scan report for localhost (127.0.0.1)
Host is up (0.00010s latency).
Not shown: 996 closed ports
PORT      STATE SERVICE
31046/tcp open  unknown
31518/tcp open  unknown
31691/tcp open  unknown
31790/tcp open  unknown
31960/tcp open  unknown

bandit16@bandit:~$ openssl s_client -connect localhost:31046
CONNECTED(00000003)
802B8AF7FF7F0000:error:0A0000F4:SSL routines:ossl_statem_client_read_transition:unexpected message:../ssl/statem/statem_clnt.c:398:
---
no peer certificate available
---
No client certificate CA names sent
---
SSL handshake has read 293 bytes and written 300 bytes
Verification: OK
---
New, (NONE), Cipher is (NONE)
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 0 (ok)
---

bandit16@bandit:~$ openssl s_client -connect localhost:31790
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 21 22:03:58 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 21 22:02:58 2023 GMT; NotAfter: Feb 21 22:03:58 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIELZxFNDANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjIxMjIwMjU4WhcNMjMwMjIxMjIwMzU4WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC8
C8jJ2//6TxiFBwjuC7+xUcu293V+n8pLxHfVnpZG9fvlOBG3nA3hm2/iNYybZNla
R58hZmfPWEKcuX7GZGvNUOAa6wOg2WYrMo1+6NCcynmCdJEabv2kemvOtBQFeV43
EUW+BW/+6903QuSHsjDewSoljGtmRGjg0oXUgyOlzGDQR/EfX7N8KGubYzZcHf+i
uZ35xMF5HQWi7Zf2ObapcbIfyjw2JWQLVqa8eDbZ4R4HKXYBLeJ4rZoYbPO1JUuX
IY6g+zV0yrgeX3EE36S4fYG/c5eixWRsA+KMYdJjtd2JTvEyyU9kSRQBNIJQOlmH
956MMGFmMqXn+kus9wgbAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQCQ
ZF30iIq43MI9neBsmpAg3W5GsZzzV/JVOPDK1BG1ynEF5hqd6SFuRRSNXXy1AN3O
jL5m5B8sIh53vzfDBhv5XgSeKDm8KPqNn9CF5yP+neVglcJh3frf6DX4yE4yntHZ
SyxWErfMX/s5P1W4NdNoph6zNWBN5EjPls9mYo4gfkUnS72FDLfyGmPan8WKUP00
hhK6TdtbcetA/9HODOD2QL82tugZvCK9qPnNHG9TkcgaJ8LW9AY/ZCwnIYsODUQi
gYSDr2Ya4GuSAp2Vn4KkaJ1+NGmE+AxUMJ0rNsKUg6JelZ6vZ4TcFNbOSqaiCOtj
5xezGlZxL+dTerQ6hBwn
-----END CERTIFICATE-----
subject=CN = localhost
issuer=CN = localhost
---
No client certificate CA names sent
Peer signing digest: SHA256
Peer signature type: RSA-PSS
Server Temp Key: X25519, 253 bits
---
SSL handshake has read 1339 bytes and written 373 bytes
Verification error: certificate has expired
---
New, TLSv1.3, Cipher is TLS_AES_256_GCM_SHA384
Server public key is 2048 bit
Secure Renegotiation IS NOT supported
Compression: NONE
Expansion: NONE
No ALPN negotiated
Early data was not sent
Verify return code: 10 (certificate has expired)
---
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 54D0256D04B37F3A98849981329DE12848EE91173FCFDC9DDDA7FD6A7C797CA6
    Session-ID-ctx:
    Resumption PSK: 818C1BCC68F71653A52EF76AA361A0CDCDF63214C9B91BDA500C186B5845301A0425BA1E6E1064C86986B27EB783076C
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - d6 2b a2 5f 29 b4 12 5c-1a 1b 28 bb f4 c8 82 45   .+._)..\..(....E
    0020 - 1a 64 4e 76 e6 d5 a5 76-56 4b 0b e1 20 bf 5c 6c   .dNv...vVK.. .\l
    0030 - 5a 11 cd 8b 3c 1c 4b a7-aa a9 86 81 7d d6 17 d2   Z...<.K.....}...
    0040 - 82 3c af 50 e4 e2 ef 76-ed ec 3d f5 7f 0e a1 53   .<.P...v..=....S
    0050 - d0 dd e5 70 2d c7 8c df-89 b0 be c0 e2 df 67 20   ...p-.........g
    0060 - a0 e0 60 ac 1c 40 68 a6-ec 49 8a 3a 50 86 9b 57   ..`..@h..I.:P..W
    0070 - c2 d4 78 8c 2d 1b 1a 25-97 5d bc e5 0f 93 5f 7b   ..x.-..%.]...._{
    0080 - 68 ed 9b c6 c9 6b 32 af-83 5d 63 15 45 3e a8 c4   h....k2..]c.E>..
    0090 - b3 29 29 b9 5c fa 8d 93-03 0f 31 e0 cf 9c 18 ff   .)).\.....1.....
    00a0 - 5b 6f 4b 0d a2 51 5c 8b-45 12 26 a6 9d bd 21 ec   [oK..Q\.E.&...!.
    00b0 - 75 0c 64 36 f0 f6 d6 1c-99 04 69 ab 4f 29 b5 ba   u.d6......i.O)..
    00c0 - a0 06 0d 29 74 03 27 67-dc a2 99 0d c7 fd 23 de   ...)t.'g......#.

    Start Time: 1677162239
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
---
Post-Handshake New Session Ticket arrived:
SSL-Session:
    Protocol  : TLSv1.3
    Cipher    : TLS_AES_256_GCM_SHA384
    Session-ID: 0DC11D3C4CE719FB01B540E8A628E27987812B74FC0D3D4BEBDED6AF05F0C2DC
    Session-ID-ctx:
    Resumption PSK: C30E913E824015434D5F6A2C134D8C7DD609D7EB5EC90363FAE349439DD5ACDA79F93265FEE736E742768D24ECF774DF
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - c6 5e 1a 4b fa 61 a1 cf-47 91 bc ee 77 38 8c 18   .^.K.a..G...w8..
    0010 - 5f 59 43 84 d0 6d ab b5-14 b8 25 91 9f fd 5e ab   _YC..m....%...^.
    0020 - dd 93 c9 bb c1 61 b3 78-d5 c9 80 5b d1 19 c0 68   .....a.x...[...h
    0030 - 36 c4 85 f5 c9 cc 3f b5-c4 fe 7d 44 7e b2 62 b2   6.....?...}D~.b.
    0040 - 74 3d 35 39 9f 6f 18 eb-e2 ff cc 34 0f 85 db 1d   t=59.o.....4....
    0050 - 6c e1 f3 79 4e 9f 67 8b-0f 67 ae ce 85 1f ef 1a   l..yN.g..g......
    0060 - c8 68 5e cf 89 5d 55 8c-3c f5 33 1a 51 43 29 a4   .h^..]U.<.3.QC).
    0070 - a2 1b 1b ee 2e 85 d9 13-64 01 16 45 c0 14 bc ea   ........d..E....
    0080 - 1e 6d 2c ca 65 67 d4 d6-41 42 03 5c 7f 6a 8a b2   .m,.eg..AB.\.j..
    0090 - 37 0b 5d 16 fd 32 b0 74-99 02 97 bc c1 d7 f4 72   7.]..2.t.......r
    00a0 - 23 31 8e 1e ab 06 10 07-92 11 b1 56 98 ba 6b 90   #1.........V..k.
    00b0 - f1 f4 d7 20 69 0a 90 8b-61 f0 74 b5 17 00 da 77   ... i...a.t....w
    00c0 - 6b 29 69 ed 66 04 0a a0-61 40 f9 c8 ed 37 f3 0c   k)i.f...a@...7..

    Start Time: 1677162239
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
JQttfApK4SeyHwDlI9SXGR50qclOAil1
Correct!
-----BEGIN RSA PRIVATE KEY-----
MIIEogIBAAKCAQEAvmOkuifmMg6HL2YPIOjon6iWfbp7c3jx34YkYWqUH57SUdyJ
imZzeyGC0gtZPGujUSxiJSWI/oTqexh+cAMTSMlOJf7+BrJObArnxd9Y7YT2bRPQ
Ja6Lzb558YW3FZl87ORiO+rW4LCDCNd2lUvLE/GL2GWyuKN0K5iCd5TbtJzEkQTu
DSt2mcNn4rhAL+JFr56o4T6z8WWAW18BR6yGrMq7Q/kALHYW3OekePQAzL0VUYbW
JGTi65CxbCnzc/w4+mqQyvmzpWtMAzJTzAzQxNbkR2MBGySxDLrjg0LWN6sK7wNX
x0YVztz/zbIkPjfkU1jHS+9EbVNj+D1XFOJuaQIDAQABAoIBABagpxpM1aoLWfvD
KHcj10nqcoBc4oE11aFYQwik7xfW+24pRNuDE6SFthOar69jp5RlLwD1NhPx3iBl
J9nOM8OJ0VToum43UOS8YxF8WwhXriYGnc1sskbwpXOUDc9uX4+UESzH22P29ovd
d8WErY0gPxun8pbJLmxkAtWNhpMvfe0050vk9TL5wqbu9AlbssgTcCXkMQnPw9nC
YNN6DDP2lbcBrvgT9YCNL6C+ZKufD52yOQ9qOkwFTEQpjtF4uNtJom+asvlpmS8A
vLY9r60wYSvmZhNqBUrj7lyCtXMIu1kkd4w7F77k+DjHoAXyxcUp1DGL51sOmama
+TOWWgECgYEA8JtPxP0GRJ+IQkX262jM3dEIkza8ky5moIwUqYdsx0NxHgRRhORT
8c8hAuRBb2G82so8vUHk/fur85OEfc9TncnCY2crpoqsghifKLxrLgtT+qDpfZnx
SatLdt8GfQ85yA7hnWWJ2MxF3NaeSDm75Lsm+tBbAiyc9P2jGRNtMSkCgYEAypHd
HCctNi/FwjulhttFx/rHYKhLidZDFYeiE/v45bN4yFm8x7R/b0iE7KaszX+Exdvt
SghaTdcG0Knyw1bpJVyusavPzpaJMjdJ6tcFhVAbAjm7enCIvGCSx+X3l5SiWg0A
R57hJglezIiVjv3aGwHwvlZvtszK6zV6oXFAu0ECgYAbjo46T4hyP5tJi93V5HDi
Ttiek7xRVxUl+iU7rWkGAXFpMLFteQEsRr7PJ/lemmEY5eTDAFMLy9FL2m9oQWCg
R8VdwSk8r9FGLS+9aKcV5PI/WEKlwgXinB3OhYimtiG2Cg5JCqIZFHxD6MjEGOiu
L8ktHMPvodBwNsSBULpG0QKBgBAplTfC1HOnWiMGOU3KPwYWt0O6CdTkmJOmL8Ni
blh9elyZ9FsGxsgtRBXRsqXuz7wtsQAgLHxbdLq/ZJQ7YfzOKU4ZxEnabvXnvWkU
YOdjHdSOoKvDQNWu6ucyLRAWFuISeXw9a/9p7ftpxm0TSgyvmfLF2MIAEwyzRqaM
77pBAoGAMmjmIJdjp+Ez8duyn3ieo36yrttF5NSsJLAbxFpdlc1gvtGCWW+9Cq0b
dxviW8+TFVEBl1O4f7HVm6EpTscdDxU+bCXWkfjuRb7Dy9GOtt9JPsX8MBTakzh3
vBgsyi/sN3RqRBcGU40fOoZyfAMT8s1m/uYv52O6IgeuZ/ujbjY=
-----END RSA PRIVATE KEY-----

closed
bandit16@bandit:~$

C:\Users\Miguel Angel\Documents>ssh -i "contrase;a.txt" bandit17@bandit.labs.overthewire.org -p 2220


```

## Notas Adicionales

| Comando | Descripcion |
| ---- | ----|
| ls| muestra los archivos|
|tr| rota la palabra como tu quieras|
|"a-zA-Z"| siginifica que voy a rotar las letras de la a - z en minusculas y masyus\
|"n-za-mN-ZA-M"| significa que la n la cambias por z, y la a por m una rotacion de 13 lugares|

password: **VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e**


## Referencias