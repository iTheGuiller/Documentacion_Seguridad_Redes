
### Descripcion

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)

### Solucion

```
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/27/fixme1.py
--2025-09-09 14:37:33--  https://artifacts.picoctf.net/c/27/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                     100%[================================================================================================>]     837  --.-KB/s    in 0s      

2025-09-09 14:37:33 (297 MB/s) - 'fixme1.py' saved [837/837]

iTheGuiller-picoctf@webshell:~$ nano fi
file       file2      files.zip  fixme1.py  
iTheGuiller-picoctf@webshell:~$ nano fixme1.py 
iTheGuiller-picoctf@webshell:~$ python3 fixme1.py 
That is correct! Here's your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}


import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x5a) + chr(0x07) + chr(0x00) + chr(0x46) + chr(0x0b) + chr(0x1a) + chr>
  

flag = str_xor(flag_enc, 'enkidu')

print('That is correct! Here\'s your flag: ' + flag)


```

### Notas

Se descarga el archivo y despues se utiliza el nano y se modifica el codigo y completa para que nos pueda arrojar la flag

## Referencias