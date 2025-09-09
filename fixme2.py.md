
### Descripcion

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)

### Solucion

```
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2025-09-09 14:59:10--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.33, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                     100%[================================================================================================>]   1.00K  --.-KB/s    in 0s      

2025-09-09 14:59:10 (903 MB/s) - 'fixme2.py' saved [1029/1029]

iTheGuiller-picoctf@webshell:~$ nano fixme2.py 

import random



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x15) + chr(0x07) + chr(0x08) + chr(0x06) + chr(0x27) + chr(0x21) + chr(0x23) + chr(0x15) + chr(0x58) + chr(0x18) + chr(0x11) + chr(0x41) + chr(0x09) + chr(0x5f) + chr>

  
flag = str_xor(flag_enc, 'enkidu')

# Check that flag is not empty
if flag == "":
  print('String XOR encountered a problem, quitting.')
else:
  print('That is correct! Here\'s your flag: ' + flag)


iTheGuiller-picoctf@webshell:~$ python3 fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
iTheGuiller-picoctf@webshell:~$ 

```

### Notas

Se tuvo que descargar el archivo y analizar para ver donde estaba erroneo, en esta ocasión fue un signo de igual

## Referencias