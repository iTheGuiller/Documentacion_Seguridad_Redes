
### Descripcion

Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/16/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/16/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/16/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

### Solucion

```
iTheGuiller-picoctf@webshell:~$ ls -la solucion.py
-rw-rw-r-- 1 iTheGuiller-picoctf iTheGuiller-picoctf 674 Sep  9 19:28 solucion.py
iTheGuiller-picoctf@webshell:~$ python3 solucion.py
¡Contraseña correcta encontrada: 865e
Hash: 1b18e1316f9218cc5b053e1cea28e02e
iTheGuiller-picoctf@webshell:~$ python3 level3.py 
Please enter correct password for flag: 865e
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_2b072a90}
iTheGuiller-picoctf@webshell:~$ 

```

### Notas
Se tuvo que crear una secuencia para poder encontrar la contraseña correcta


## Referencias