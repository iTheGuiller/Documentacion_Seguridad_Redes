
### Descripcion

Unzip this archive and find the file named 'uber-secret.txt'

- [Download zip file](https://artifacts.picoctf.net/c/501/files.zip)

### Solucion

```
iTheGuiller-picoctf@webshell:~$ ls
Addadshashanammu  Addadshashanammu.zip  README.txt  big-zip-files  big-zip-files.zip  enc_flag  file  file2  files.zip  flag  ltdis.sh  salida.txt  static  strings  warm
iTheGuiller-picoctf@webshell:~$ strings files.zip | grep pico
picoCTF{f1nd_15_f457_ab443fd1}
iTheGuiller-picoctf@webshell:~$ 

```

### Notas

El comando `strings files.zip | grep pico` busca y muestra todas las cadenas de texto legible dentro del archivo `files.zip` que contienen la palabra "pico".

- `strings`: extrae texto legible de archivos binarios.
- `grep pico`: filtra las líneas que contienen la palabra "pico".

## Referencias