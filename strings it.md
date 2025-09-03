
### Descripcion

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings) without running it?

### Solucion
Se descarga el archivo y despues se lee sin abrirlo con el comando strings strings y con el comando "grep" buscar la flag especifica picoCTF.


```
iTheGuiller-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings > file
--2025-09-03 16:35:31--  https://jupiter.challenges.picoctf.org/static/94d00153b0057d37da225ee79a846c62/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                       100%[================================================================================================>] 757.84K  1.86MB/s    in 0.4s    

2025-09-03 16:35:31 (1.86 MB/s) - 'strings' saved [776032/776032]

iTheGuiller-picoctf@webshell:~$ ls
README.txt  file  flag  salida.txt  strings
iTheGuiller-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_d66c7bb7}
iTheGuiller-picoctf@webshell:~$ 

```

### Notas

El comando `strings strings | grep picoCTF` busca el texto "picoCTF" dentro del contenido legible de un archivo llamado `strings`.

- **`strings`**: Extrae todas las secuencias de texto legible del archivo llamado `strings`. Esto es útil cuando el archivo `strings` es binario o no es directamente legible.
- **`| grep picoCTF`**: Filtra el resultado para mostrar solo las líneas que contienen la palabra "picoCTF", que a menudo está relacionada con retos de captura de la bandera (CTF) en competencias de seguridad informática.[](https://github.com/armandoportillo0101/Seguridad-de-Redes/blob/main/Plantilla.md#notas-adicionales)

## Referencias