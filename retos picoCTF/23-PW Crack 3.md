## Objetivo
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/28/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/28/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/28/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
## Hints

## Solución

```
  GNU nano 6.2                                            level3.py                                                         m = hashlib.md5()
    m.update(pw_bytes)
    return m.digest()


def level_3_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    user_pw_hash = hash_pw(user_pw)

    if( user_pw_hash == correct_pw_hash ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_3_pw_check()


# The strings below are 7 possibilities for the correct password.
#   (Only 1 is correct)
pos_pw_list = ["6997", "3ac8", "f0ac", "4b17", "ec27", "4e66", "865e"]

C:\Users\Miguel Angel\Downloads>level3.py
Please enter correct password for flag: 6997
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}

```

## Notas Adicionales

Usando la lista y los números, probamos cada uno de las palabras que hay. el primero es 6997 

## Referencias