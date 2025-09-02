

### Descripcion
This file has a flag in plain sight (aka "in-the-clear"). [Download flag](https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag).

### Solucion
Descargar el archivo y después utilizar el comando cat para buscar la bandera

```
iTheGuiller-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
--2025-09-01 17:11:49--  https://mercury.picoctf.net/static/217686fc11d733b80be62dcfcfca6c75/flag
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 34 [application/octet-stream]
Saving to: 'flag'

flag                                          100%[================================================================================================>]      34  --.-KB/s    in 0s      

2025-09-01 17:11:49 (19.1 MB/s) - 'flag' saved [34/34]

iTheGuiller-picoctf@webshell:~$ grep 'in-the-clear' flag
iTheGuiller-picoctf@webshell:~$ cat flag
picoCTF{s4n1ty_v3r1f13d_b5aeb3dd}
```
### Notas
El comando cat sirve para mostrar el contenido de un archivo en la terminal.

## Referencias
