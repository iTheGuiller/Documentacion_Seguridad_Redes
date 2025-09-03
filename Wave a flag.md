
### Descripcion

Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm) has extraordinarily helpful information...

### Solucion

```
iTheGuiller-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm > file
--2025-09-03 16:43:18--  https://mercury.picoctf.net/static/b28b6021d6040b086c2226ebeb913bc2/warm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 10936 (11K) [application/octet-stream]
Saving to: 'warm'

warm                                          100%[================================================================================================>]  10.68K  --.-KB/s    in 0s      

2025-09-03 16:43:18 (392 MB/s) - 'warm' saved [10936/10936]

iTheGuiller-picoctf@webshell:~$ ls
README.txt  file  flag  salida.txt  strings  warm
iTheGuiller-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=b11c22752c901adc13ba1ce86eda9d5516f22763, with debug_info, not stripped
iTheGuiller-picoctf@webshell:~$ chmod +x warm
iTheGuiller-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_d6969390}
iTheGuiller-picoctf@webshell:~$ 
```

### Notas

### 1. `chmod +x warm`

[](https://github.com/armandoportillo0101/Seguridad-de-Redes/blob/main/Problemas_parcial1_pico/Wave%20a%20flag.md#1-chmod-x-warm)

- **`chmod`**: Es el comando que cambia los permisos de un archivo en sistemas tipo Unix (Linux, macOS).
- **`+x`**: Añade el permiso de ejecución (execute) al archivo.
- **`warm`**: Es el nombre del archivo al que le estás asignando el permiso de ejecución.

En resumen, `chmod +x warm` hace que el archivo `warm` sea ejecutable, permitiendo que puedas correrlo como un programa.

### 2. `./warm -h`

[](https://github.com/armandoportillo0101/Seguridad-de-Redes/blob/main/Problemas_parcial1_pico/Wave%20a%20flag.md#2-warm--h)

- **`./warm`**: Ejecuta el archivo llamado `warm` desde el directorio actual. El prefijo `./` indica que el archivo está en el directorio en el que te encuentras.
- **`-h`**: Es una opción que típicamente muestra la ayuda del programa o información sobre cómo usarlo. Muchas aplicaciones incluyen la opción `-h` (o `--help`) para ofrecer instrucciones de uso.[](https://github.com/armandoportillo0101/Seguridad-de-Redes/blob/main/Plantilla.md#notas-adicionales)

## Referencias