
### Descripcion

Run the Python script and convert the given number from decimal to binary to get the flag.[Download Python script](https://artifacts.picoctf.net/c/24/convertme.py)

### Solucion

```
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2025-09-09 14:16:20--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.72, 3.170.131.77, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py                                  100%[================================================================================================>]   1.16K  --.-KB/s    in 0s      

2025-09-09 14:16:20 (1.18 GB/s) - 'convertme.py' saved [1189/1189]

iTheGuiller-picoctf@webshell:~$ ls
Addadshashanammu      README.txt     big-zip-files.zip  codebook.txt  enc_flag  file2      flag      runme.py    static   warm
Addadshashanammu.zip  big-zip-files  code.py            convertme.py  file      files.zip  ltdis.sh  salida.txt  strings
iTheGuiller-picoctf@webshell:~$ python3 convertme.py
If 100 is in decimal base, what is it in binary base?
Answer: 1100100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
iTheGuiller-picoctf@webshell:~$ 

```

### Notas

Se tuvo que convertir el numero 100 en decimal para poder tener la flag

## Referencias