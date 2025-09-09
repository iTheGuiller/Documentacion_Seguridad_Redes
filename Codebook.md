
### Descripcion

Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/1/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/1/codebook.txt)

### Solucion

```
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py
--2025-09-09 14:12:23--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... }3.170.131.18, 3.170.131.72, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                                       100%[================================================================================================>]   1.25K  --.-KB/s    in 0s      

2025-09-09 14:12:23 (837 MB/s) - 'code.py' saved [1278/1278]

iTheGuiller-picoctf@webshell:~$ }ls
-bash: }ls: command not found
iTheGuiller-picoctf@webshell:~$ python3 code.py
Couldn't find codebook.txt. Did you download that file into the same directory as this script?
iTheGuiller-picoctf@webshell:~$ ls
Addadshashanammu      README.txt     big-zip-files.zip  enc_flag  file2      flag      runme.py    static   warm
Addadshashanammu.zip  big-zip-files  code.py            file      files.zip  ltdis.sh  salida.txt  strings
iTheGuiller-picoctf@webshell:~$ python3 code.py 
Couldn't find codebook.txt. Did you download that file into the same directory as this script?
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2025-09-09 14:13:41--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.77, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt                                  100%[================================================================================================>]      27  --.-KB/s    in 0s      

2025-09-09 14:13:41 (1.16 MB/s) - 'codebook.txt' saved [27/27]

iTheGuiller-picoctf@webshell:~$ python3 code.py 
picoCTF{c0d3b00k_455157_d9aa2df2}
iTheGuiller-picoctf@webshell:~$ 

```

### Notas

El comando `python3 code.py` ejecuta el script `code.py` usando Python 3

## Referencias