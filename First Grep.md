

### Descripcion
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file)? This would be really tedious to look through manually, something tells me there is a better way.

### Solucion
Descargar el archivo en la consola 
Aplicar el comando gref

```
iTheGuiller-picoctf@webshell:~$ wc -file
wc: invalid option -- 'f'
Try 'wc --help' for more information.
iTheGuiller-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
--2025-09-01 17:08:36--  https://jupiter.challenges.picoctf.org/static/315d3325dc668ab7f1af9194f2de7e7a/file
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 14551 (14K) [application/octet-stream]
Saving to: 'file'

file                                          100%[================================================================================================>]  14.21K  --.-KB/s    in 0s      

2025-09-01 17:08:36 (440 MB/s) - 'file' saved [14551/14551]

iTheGuiller-picoctf@webshell:~$ wc file
    6   317 14551 file
iTheGuiller-picoctf@webshell:~$ grep 'picoCTF' file
picoCTF{grep_is_good_to_find_things_f77e0797}
iTheGuiller-picoctf@webshell:~$ 
```

### Notas
no sabia que se descargaba con wget y wc cuenta la lineas de texto

## Referencias
https://webshell.picoctf.org