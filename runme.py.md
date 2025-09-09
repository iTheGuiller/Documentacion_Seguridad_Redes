
### Descripcion
Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)


### Solucion

```
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2025-09-09 14:08:13--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.77, 3.170.131.18, 3.170.131.33, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.77|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                      100%[================================================================================================>]     270  --.-KB/s    in 0s      

2025-09-09 14:08:13 (71.3 MB/s) - 'runme.py' saved [270/270]

iTheGuiller-picoctf@webshell:~$ cat runme.py
#!/usr/bin/python3
################################################################################
# Python script which just prints the flag
################################################################################

flag ='picoCTF{run_s4n1ty_run}'
print(flag)

iTheGuiller-picoctf@webshell:~$ 

```

### Notas

Se decarga el archivo python y se corrio para que nos diera la bandera 

## Referencias