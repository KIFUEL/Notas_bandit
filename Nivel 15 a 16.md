## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL encryption.

**Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -ign_eof and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…**
## Datos de Acceso
host :  **bandit.labs.overthewire.org** port 2220
username is **bandit15**
ssh:  bandit15@bandit.labs.overthewire.org -p 2220
password: **jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt**
## Solución

``` bash
bandit14@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Cant use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 24 22:59:04 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 24 22:59:04 2023 GMT
verify return:1
---
Certificate chain
 0 s:CN = localhost
   i:CN = localhost
   a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
   v:NotBefore: Feb 24 22:58:04 2023 GMT; NotAfter: Feb 24 22:59:04 2023 GMT
---
Server certificate
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEdtHsNjANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjI0MjI1ODA0WhcNMjMwMjI0MjI1OTA0WjAUMRIwEAYD
VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQCx
mrCINhzIGCIeMR5GsleGkWUZWNcLl1D3FFa0OwDgYG0lj4VP3fC2jf7SJ8DbMdGT
jqyOhsM+LZhKWPJ+NH60lzWTeYq6/pe2OMFhZ6bbd84coT7Fo7Evjk4bye2+qYsH
J6MR7Gk+bhL9U4KpCVOpZwHitiC4ZbX+s7n8PHQsfMeQfhSS7J+Xa0vTw3KQoVCg
3BhKTD9bt3gXVfGNaIvECku2sCECDkFyCR5+AqswPHCT7QK8Q3sb9gbA0/zhWbXb
h4RVpbwm+NqmDivMxPVSH+J6NzgmBpLTpeFsN05rlN9CdzRP9l+tLCJnf1irtKMI
0KkVzlGMg/vwLKYA0G5pAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBx
vsPCAfYKiOZH0RDDB18SoiFpjkw3A9lSM14tvFlYsEdx31DvJNwc6QT/E8uOV2sB
Kl4wGwJQPJ7VT93CClFN3je9drqlNryCm+P4VO1Fhay8JIb6PyW0z4WCIlJqCRKT
68SPozIEfx/lwquR+MPyopny7tIlA1IZN4aF5yA+Gi570zC7UtdRBVyfGrdANeS8
5pmwA2NzxauCh3QJc2jWYVk4qmmTsLJBgElaFN1QrZHk60rxaUjS4rFnsSYZ/d4n
kmj3TPpRidAxlDM5qnXqD7fcBNy3s7XXk40ygWS/GsJJx38sHr0yFmMV7l0QKVBC
rsP6Hy0UaGAkUNBjj/Fi
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
    Session-ID: 2CD976C7989E73215853E4F79E2B0B20611CD750BFE696932912AE8141DE4B4B
    Session-ID-ctx:
    Resumption PSK: AD4845E92E2ADEC4AB772EB6FB9851D06AFCFE8A5782E577552606391E4379B1799BDBEEF68C8B4309714899E18A14E4
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cb 00 ae d3 fc cf 12 aa-e1 f0 d3 ef 6c 0e a6 aa   ............l...
    0010 - 76 34 c7 04 39 6f 36 6d-66 0d c8 b1 57 94 f6 a1   v4..9o6mf...W...
    0020 - 09 c1 cb 85 90 37 7f bf-ee ca 3e 45 e4 8f b5 3e   .....7....>E...>
    0030 - b4 7e d9 65 7a 5b d0 df-be ed f2 65 db 56 4e 3f   .~.ez[.....e.VN?
    0040 - 83 87 9d a8 a8 72 54 08-23 db 6a 66 48 13 31 c2   .....rT.#.jfH.1.
    0050 - 11 c3 f4 7a 1a 46 58 db-2b a4 8d b4 8d 1b e6 ab   ...z.FX.+.......
    0060 - d4 ce f0 8c 6d d3 68 2f-ae f2 f2 14 c5 ac 23 36   ....m.h/......#6
    0070 - df b1 a8 89 ff de 33 54-84 6c 69 9e f4 5a 94 83   ......3T.li..Z..
    0080 - 52 bd 6d 28 d0 e3 36 66-c2 96 b8 12 18 cd 0f 0e   R.m(..6f........
    0090 - 2b 85 f3 28 01 e7 06 c8-ad e3 45 b3 b4 79 6d bb   +..(......E..ym.
    00a0 - e4 20 ae fd 99 fb 44 45-a7 0e 2f 11 0b 83 78 d2   . ....DE../...x.
    00b0 - fa 3a 90 6e 84 dc 14 bf-01 e5 3b 14 fc 9a 62 80   .:.n......;...b.
    00c0 - 83 07 a3 fd 67 b5 fb c9-3b cf e5 ec 97 3f c3 3f   ....g...;....?.?

    Start Time: 1677461350
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
    Session-ID: EF6E03C03DCAF6A5EF289FC06AAC6889E5D0150E9E9755316445174416F49ED9
    Session-ID-ctx:
    Resumption PSK: 3B81BFE3B58BDBAABD51B8F84891E6C4BCBA845D2A1DB7677EC07307B6E62216479101F1A925136793A4B7DC8ECE32F3
    PSK identity: None
    PSK identity hint: None
    SRP username: None
    TLS session ticket lifetime hint: 7200 (seconds)
    TLS session ticket:
    0000 - cb 00 ae d3 fc cf 12 aa-e1 f0 d3 ef 6c 0e a6 aa   ............l...
    0010 - 8a 86 c2 33 c8 df 88 dd-53 d3 89 73 1b 96 f6 d4   ...3....S..s....
    0020 - 75 a4 39 dd 1b 1c 05 ed-0e ac f5 42 ec 86 c3 16   u.9........B....
    0030 - c5 73 06 e0 01 23 85 55-b5 1e 32 80 28 59 3b 5c   .s...#.U..2.(Y;\
    0040 - 01 bd bf 37 0d 82 99 2d-b2 5d 81 d5 53 fa 7e 46   ...7...-.]..S.~F
    0050 - ff 74 67 bd 2b 12 59 ff-71 1e fb bb 58 a1 4b 95   .tg.+.Y.q...X.K.
    0060 - c1 29 de e3 b1 a3 c5 80-df 96 c2 14 3d 1b 03 65   .)..........=..e
    0070 - 0d 18 a1 d1 50 ac e2 5d-bc 63 1a fd 01 77 d8 50   ....P..].c...w.P
    0080 - 34 e4 29 fa db 87 b0 fd-d7 e8 dc 01 5d 8b 29 b9   4.).........].).
    0090 - a2 b1 34 66 1d 6b 2a 3c-99 ba 09 f5 73 e1 19 f2   ..4f.k*<....s...
    00a0 - c6 93 a5 43 26 be fc 07-e5 2f 3e 25 1c 00 19 8c   ...C&..../>%....
    00b0 - 55 91 62 c4 24 2f 18 82-b1 59 dc d9 97 18 36 eb   U.b.$/...Y....6.
    00c0 - c4 e3 df 55 90 b8 3b e3-c3 2d 95 12 ae 1a 0b 20   ...U..;..-.....

    Start Time: 1677461350
    Timeout   : 7200 (sec)
    Verify return code: 10 (certificate has expired)
    Extended master secret: no
    Max Early Data: 0
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1

closed
bandit14@bandit:~$

```

## Notas Adicionales

password: **JQttfApK4SeyHwDlI9SXGR50qclOAil1**


## Referencias