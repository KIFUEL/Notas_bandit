## Descripción 

This vault uses for-loops and byte arrays. The source code for this vault is here: [VaultDoor3.java](https://jupiter.challenges.picoctf.org/static/a4018cec1446761cb2e8cce05db925fa/VaultDoor3.java)

## Hints
Make a table that contains each value of the loop variables and the corresponding buffer index that it writes to.
## Solución
modificamos la funcion Checkpassword para que muestre el contenido del buffer que es la palabra de la bandera 
```
public boolean checkPassword(String password) {

        if (password.length() != 32) {

            return false;

        }

        char[] buffer = new char[32];

        int i;

        for (i=0; i<8; i++) {

            buffer[i] = password.charAt(i);

        }

        for (; i<16; i++) {

            buffer[i] = password.charAt(23-i);

        }

        for (; i<32; i+=2) {

            buffer[i] = password.charAt(46-i);

        }

        for (i=31; i>=17; i-=2) {

            buffer[i] = password.charAt(i);

        }

        String s = new String(buffer);

        System.out.println(s);

        return s.equals("jU5t_a_sna_3lpm12g94c_u_4_m7ra41");

    }

}


```


## Bandera
picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21} 