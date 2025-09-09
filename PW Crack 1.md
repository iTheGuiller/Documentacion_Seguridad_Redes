
### Descripcion

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/11/level1.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/11/level1.flag.txt.enc) in the same directory too.

### Solucion

```
iTheGuiller-picoctf@webshell:~$ ls
Addadshashanammu      README.txt     big-zip-files.zip  codebook.txt  enc_flag  file2      fixme1.py  flag                 level1.py  runme.py    static   warm
Addadshashanammu.zip  big-zip-files  code.py            convertme.py  file      files.zip  fixme2.py  level1.flag.txt.enc  ltdis.sh   salida.txt  strings
iTheGuiller-picoctf@webshell:~$ cat level1.py
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


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
iTheGuiller-picoctf@webshell:~$ nano level1.
level1.flag.txt.enc  level1.py            
iTheGuiller-picoctf@webshell:~$ nano level1.flag.txt.enc 
iTheGuiller-picoctf@webshell:~$ python3 level1.py 
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
```

### Notas

Se tuvieron que descargar los dos archivos, despues entre a nano para ver el archivo de la contraseña y despues ejecute el python y me dio el flag

## Referencias