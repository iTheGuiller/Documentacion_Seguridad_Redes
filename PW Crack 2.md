
### Descripcion

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/15/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/15/level2.flag.txt.enc) in the same directory too.

### Solucion

```

iTheGuiller-picoctf@webshell:~$ ls
Addadshashanammu      README.txt     big-zip-files.zip  codebook.txt  enc_flag  file2      fixme1.py  flag                 level1.py            level2.py  runme.py    static   warm
Addadshashanammu.zip  big-zip-files  code.py            convertme.py  file      files.zip  fixme2.py  level1.flag.txt.enc  level2.flag.txt.enc  ltdis.sh   salida.txt  strings
iTheGuiller-picoctf@webshell:~$ cat level2.py
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])
###############################################################################

flag_enc = open('level2.flag.txt.enc', 'rb').read()



def level_2_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == chr(0x33) + chr(0x39) + chr(0x63) + chr(0x65) ):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_2_pw_check()
iTheGuiller-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: 39ce
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_502ec42e}
iTheGuiller-picoctf@webshell:~$ 

- `chr(0x33)`: El hexadecimal `0x33` es el número decimal 51, que corresponde al carácter **'3'**.
    
- `chr(0x39)`: El hexadecimal `0x39` es el número decimal 57, que corresponde al carácter **'9'**.
    
- `chr(0x63)`: El hexadecimal `0x63` es el número decimal 99, que corresponde al carácter **'c'**.
    
- `chr(0x65)`: El hexadecimal `0x65` es el número decimal 101, que corresponde al carácter **'e'**.
  
  el resultado final es `39ce`.
  
```

### Notas

Se descargaron los 2 archivos y se examino unno con nano para ver como funcionaba, una vez ahi se observa la logica que se ocupa para dar la flag y se trabajo sobre ello.

## Referencias