

### Descripcion

Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/473/enc_flag).

### Solucion

```
iTheGuiller-picoctf@webshell:~$ ls   
Addadshashanammu  Addadshashanammu.zip  README.txt  file  file2  flag  ltdis.sh  salida.txt  static  strings  warm
iTheGuiller-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/473/enc_flag
--2025-09-03 17:35:29--  https://artifacts.picoctf.net/c/473/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.33, 3.170.131.72, 3.170.131.18, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.33|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag                                      100%[================================================================================================>]     349  --.-KB/s    in 0s      

2025-09-03 17:35:29 (122 MB/s) - 'enc_flag' saved [349/349]

iTheGuiller-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt  enc_flag  file  file2  flag  ltdis.sh  salida.txt  static  strings  warm
iTheGuiller-picoctf@webshell:~$ cat enc_flag
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbHBWV0VKVVZGWm9RMlZzV2tWUmJFNVNDbUpXV25wWmExSmhWMGRHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
iTheGuiller-picoctf@webshell:~$ strings enc_flag | grep pico
iTheGuiller-picoctf@webshell:~$ base64 -d enc_flag
VjFSQ2EyTXlSblJUV0dSVllrWmFWRmx0TlZOalJtUlhZVVU1YVZKVVZuaFdWekZoWVZkR2NrNVVX
bUZTVmtwUVdWUkdibVZXVm5WUgpiSEJzWVRCd2VWVXhXbXBOUlRWSFdqTnNWZ3BYUjFKeVZGZHdW
MlZzVWxaVmJFNW9UVVJDTlZaWE1XRlpVWEJUVFZoQ2VsWkVRbE5SCmJWWnpZa1JhV0dGdGVFVlhi
bTkzVDFWT2JsQlVNRXNLCg==
iTheGuiller-picoctf@webshell:~$ base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_dfe803c6}
iTheGuiller-picoctf@webshell:~$ 
```

### Notas

El comando `base64 -d enc_flag | base64 -d | base64 -d | base64 -d | base64 -d | base64 -d` decodifica un archivo o cadena codificada en base64 múltiples veces.

- `base64 -d`: decodifica datos en formato base64.
- `enc_flag`: es el archivo o texto codificado en base64 que se está procesando.
- Las tuberías (`|`) encadenan las decodificaciones para aplicar el proceso repetidamente.

En este caso, el archivo `enc_flag` se decodifica 6 veces consecutivas hasta revelar el contenido original. Cada ejecución toma el resultado de la anterior hasta llegar al dato fina

## Referencias